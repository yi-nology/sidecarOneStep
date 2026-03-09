# SidecarOneStep MCP (stdio) 接口文档

本文档说明如何通过 **stdio** 方式连接 SidecarOneStep 的 MCP 服务，并调用工具。

## 启动方式

通过 `mcp` 子命令启动 MCP 服务（stdio）：

```bash
SidecarOneStep mcp
```

> 当 Settings 中 **启用 MCP (stdio)** 关闭时，`mcp` 会直接退出并提示开启。

## 传输协议

- 传输方式：stdio（stdin/stdout）
- 协议：JSON-RPC 2.0
- 每行一条 JSON

请求示例：
```json
{"jsonrpc":"2.0","id":1,"method":"tools/list"}
```

响应示例：
```json
{"jsonrpc":"2.0","id":1,"result":{"tools":[...]}}
```

## 初始化流程

1. `initialize`
2. `initialized`
3. `tools/list`
4. `tools/call`

`initialize` 示例：
```json
{"jsonrpc":"2.0","id":1,"method":"initialize","params":{"protocolVersion":"2024-11-05"}}
```

## 工具列表

### 1) list_devices
列出可用设备。

**请求**
```json
{"jsonrpc":"2.0","id":2,"method":"tools/call","params":{"name":"list_devices","arguments":{}}}
```

**返回**（text 内容为 JSON 数组）
```json
{"jsonrpc":"2.0","id":2,"result":{"content":[{"type":"text","text":"[\n  \"XX的iPad Pro\"\n]"}]}}
```

---

### 2) connect_device
同步连接设备（可能阻塞）。

**请求**
```json
{"jsonrpc":"2.0","id":3,"method":"tools/call","params":{"name":"connect_device","arguments":{"device_name":"XX的iPad Pro","wired":false}}}
```

**返回**
```json
{"jsonrpc":"2.0","id":3,"result":{"content":[{"type":"text","text":"XX的iPad Pro"}]}}
```

---

### 3) connect_device_async
异步连接（推荐，避免 15s 超时）。返回 `job_id`。

**请求**
```json
{"jsonrpc":"2.0","id":4,"method":"tools/call","params":{"name":"connect_device_async","arguments":{"device_name":"XX的iPad Pro","wired":false}}}
```

**返回**
```json
{"jsonrpc":"2.0","id":4,"result":{"content":[{"type":"text","text":"{\n  \"job_id\" : \"<uuid>\"\n}"}]}}
```

---

### 4) get_job_status
查询异步连接结果。

**请求**
```json
{"jsonrpc":"2.0","id":5,"method":"tools/call","params":{"name":"get_job_status","arguments":{"job_id":"<uuid>"}}}
```

**返回**（status: pending / success / failed / cancelled / not_found）
```json
{"jsonrpc":"2.0","id":5,"result":{"content":[{"type":"text","text":"{\n  \"id\" : \"<uuid>\",\n  \"type\" : \"connect\",\n  \"device_name\" : \"XX的iPad Pro\",\n  \"wired\" : false,\n  \"status\" : \"success\",\n  \"result\" : \"XX的iPad Pro\",\n  \"error\" : null,\n  \"created_at\" : \"2026-03-09T12:34:56.789Z\"\n}"}]}}
```

---

### 5) cancel_job
取消等待中的任务。

**请求**
```json
{"jsonrpc":"2.0","id":6,"method":"tools/call","params":{"name":"cancel_job","arguments":{"job_id":"<uuid>"}}}
```

**返回**
```json
{"jsonrpc":"2.0","id":6,"result":{"content":[{"type":"text","text":"{\n  \"job_id\" : \"<uuid>\",\n  \"cancelled\" : true\n}"}]}}
```

---

### 6) disconnect_device
断开设备。

**请求**
```json
{"jsonrpc":"2.0","id":7,"method":"tools/call","params":{"name":"disconnect_device","arguments":{"device_name":"XX的iPad Pro"}}}
```

---

### 7) start_http_server
启动 HTTP 服务。

**请求**
```json
{"jsonrpc":"2.0","id":8,"method":"tools/call","params":{"name":"start_http_server","arguments":{"port":8765}}}
```

---

### 8) stop_http_server
停止 HTTP 服务。

**请求**
```json
{"jsonrpc":"2.0","id":9,"method":"tools/call","params":{"name":"stop_http_server","arguments":{}}}
```

---

### 9) get_status
获取状态。

**请求**
```json
{"jsonrpc":"2.0","id":10,"method":"tools/call","params":{"name":"get_status","arguments":{}}}
```

**返回**（text 内容为 JSON）
```json
{"jsonrpc":"2.0","id":10,"result":{"content":[{"type":"text","text":"{\n  \"server_running\" : true,\n  \"server_port\" : 8765,\n  \"active_device\" : \"XX的iPad Pro\",\n  \"active_wired\" : false\n}"}]}}
```

---

### 10) get_logs
读取最近日志。

**请求**
```json
{"jsonrpc":"2.0","id":11,"method":"tools/call","params":{"name":"get_logs","arguments":{"limit":50}}}
```

---

## 建议流程

1. `list_devices`
2. `connect_device_async`
3. 轮询 `get_job_status` 直到 `success`

## 常见问题

- **connect_device 超时**：请用 `connect_device_async`
- **设备不在列表**：确认 iPad 解锁、同一 Apple ID、已启用 Sidecar
