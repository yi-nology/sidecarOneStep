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
{"jsonrpc":"2.0","id":2,"result":{"content":[{"type":"text","text":"[\n  \"张易的iPad Pro\"\n]"}]}}
```

---

### 2) connect_device
同步连接设备（可能阻塞）。

**请求**
```json
{"jsonrpc":"2.0","id":3,"method":"tools/call","params":{"name":"connect_device","arguments":{"device_name":"张易的iPad Pro","wired":false}}}
```

**返回**
```json
{"jsonrpc":"2.0","id":3,"result":{"content":[{"type":"text","text":"张易的iPad Pro"}]}}
```

---

### 3) connect_device_async
异步连接（推荐，避免 15s 超时）。返回 `job_id`。

**请求**
```json
{"jsonrpc":"2.0","id":4,"method":"tools/call","params":{"name":"connect_device_async","arguments":{"device_name":"张易的iPad Pro","wired":false}}}
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
{"jsonrpc":"2.0","id":5,"result":{"content":[{"type":"text","text":"{\n  \"id\" : \"<uuid>\",\n  \"type\" : \"connect\",\n  \"device_name\" : \"张易的iPad Pro\",\n  \"wired\" : false,\n  \"status\" : \"success\",\n  \"result\" : \"张易的iPad Pro\",\n  \"error\" : null,\n  \"created_at\" : \"2026-03-09T12:34:56.789Z\"\n}"}]}}
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
{"jsonrpc":"2.0","id":7,"method":"tools/call","params":{"name":"disconnect_device","arguments":{"device_name":"张易的iPad Pro"}}}
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
{"jsonrpc":"2.0","id":10,"result":{"content":[{"type":"text","text":"{\n  \"server_running\" : true,\n  \"server_port\" : 8765,\n  \"active_device\" : \"张易的iPad Pro\",\n  \"active_wired\" : false\n}"}]}}
```

---

### 10) get_logs
读取最近日志。

**请求**
```json
{"jsonrpc":"2.0","id":11,"method":"tools/call","params":{"name":"get_logs","arguments":{"limit":50}}}
```

---

### 11) virtual_display_status
获取虚拟显示器状态。

**请求**
```json
{"jsonrpc":"2.0","id":12,"method":"tools/call","params":{"name":"virtual_display_status","arguments":{}}}
```

**返回**（text 内容为 JSON）
```json
{"jsonrpc":"2.0","id":12,"result":{"content":[{"type":"text","text":"{\n  \"enabled\" : true,\n  \"active\" : true,\n  \"definition_id\" : 10\n}"}]}}
```

**字段说明**
- `enabled`: 是否在设置中启用了虚拟显示器
- `active`: 虚拟显示器是否正在运行
- `definition_id`: 当前选择的尺寸预设 ID

---

### 12) list_virtual_display_sizes
列出可用虚拟显示器尺寸。

**请求**
```json
{"jsonrpc":"2.0","id":13,"method":"tools/call","params":{"name":"list_virtual_display_sizes","arguments":{}}}
```

**返回**（text 内容为 JSON 数组）
```json
{"jsonrpc":"2.0","id":13,"result":{"content":[{"type":"text","text":"[\n  {\n    \"id\" : 10,\n    \"description\" : \"16:9 (HD/4K/5K/6K)\"\n  }\n]"}]}}
```

**可用尺寸预设**（部分常用）
| ID  | 描述 |
|-----|------|
| 10  | 16:9 (HD/4K/5K/6K) - 默认 |
| 20  | 16:10 (W*XGA) |
| 30  | 4:3 (VGA, iPad) |
| 40  | 17:9 (4K-DCI) |
| 50  | 21.3:9 (UW-HD/4K/5K) |
| 60  | 21.5:9 (UW-QHD) |
| 70  | 24:10 (UW-QHD+) |
| 80  | 32:10 (D-W*XGA) |
| 90  | 32:9 (D-HD/QHD) |
| 100 | 1:1 (Square) |
| 110 | 9:16 (Portrait) |
| 380 | iPad mini 6 (2266x1488) |
| 390 | iPad Air 11 (2360x1640) |
| 400 | iPad Pro 11 (2388x1668) |
| 410 | iPad Pro 11 (2420x1668) |
| 420 | iPad Air 13 (2732x2048) |
| 430 | iPad Pro 12.9 (2732x2048) |
| 440 | iPad Pro 13 (2752x2064) |

---

### 13) set_virtual_display_size
设置虚拟显示器尺寸（definition_id）。

**请求**
```json
{"jsonrpc":"2.0","id":14,"method":"tools/call","params":{"name":"set_virtual_display_size","arguments":{"definition_id":10}}}
```

**参数说明**
- `definition_id`: 尺寸预设 ID（整数），使用 `list_virtual_display_sizes` 获取可用 ID

**返回**
```json
{"jsonrpc":"2.0","id":14,"result":{"content":[{"type":"text","text":"{\n  \"ok\" : true,\n  \"definition_id\" : 10\n}"}]}}
```

**注意**：如果虚拟显示器已启用，设置新尺寸会自动重新创建显示器。

---

### 14) enable_virtual_display
开启虚拟显示器（使用当前选择的尺寸）。

**请求**
```json
{"jsonrpc":"2.0","id":15,"method":"tools/call","params":{"name":"enable_virtual_display","arguments":{}}}
```

**返回**
```json
{"jsonrpc":"2.0","id":15,"result":{"content":[{"type":"text","text":"{\n  \"ok\" : true,\n  \"definition_id\" : 10\n}"}]}}
```

**失败返回示例**
```json
{"jsonrpc":"2.0","id":15,"result":{"content":[{"type":"text","text":"{\n  \"ok\" : false,\n  \"definition_id\" : 10\n}"}]}}
```

**注意**：启用失败通常是权限或系统版本问题。

---

### 15) disable_virtual_display
关闭虚拟显示器。

**请求**
```json
{"jsonrpc":"2.0","id":16,"method":"tools/call","params":{"name":"disable_virtual_display","arguments":{}}}
```

**返回**
```json
{"jsonrpc":"2.0","id":16,"result":{"content":[{"type":"text","text":"{\n  \"ok\" : true\n}"}]}}
```

---

## 建议流程

### Sidecar 设备连接
1. `list_devices` - 列出可用设备
2. `connect_device_async` - 异步连接（避免超时）
3. 轮询 `get_job_status` 直到 `status` 为 `success`

### 虚拟显示器操作
1. `list_virtual_display_sizes` - 查看可用尺寸
2. `set_virtual_display_size` - 选择尺寸（可选，默认 ID 10）
3. `enable_virtual_display` - 启用虚拟显示器
4. `virtual_display_status` - 检查状态
5. `disable_virtual_display` - 不用时关闭

**推荐尺寸**
- 默认使用 ID 10 (16:9 通用比例)
- iPad 用户推荐 ID 380-440（匹配实际设备分辨率）
- 超宽屏需求可用 ID 50-90

## 常见问题

### Sidecar 连接问题
- **connect_device 超时**：使用 `connect_device_async` 避免阻塞
- **设备不在列表**：确认 iPad 已解锁、同一 Apple ID、Sidecar 已启用
- **连接失败**：检查网络连接、蓝牙状态、设备距离

### 虚拟显示器问题
- **启用失败**：检查系统权限（屏幕录制权限）、macOS 版本（需 12.0+）
- **显示器不显示**：检查系统偏好设置 → 显示器
- **性能问题**：尝试降低分辨率（选择较小尺寸预设）

### MCP 服务问题
- **mcp 命令退出**：检查设置中是否启用了 MCP (stdio)
- **工具调用无响应**：检查 JSON-RPC 格式、id 唯一性
- **日志查看**：使用 `get_logs` 工具查看最近操作记录

## 版本信息

- **当前版本**: 1.4.0
- **新增功能**: 虚拟显示器支持（v1.4.0）
- **MCP 工具总数**: 15 个
