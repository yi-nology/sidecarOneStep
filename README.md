# SidecarOneStep（随航一步）

<p align="center">
  <img src="assets/icon.png" alt="SidecarOneStep Logo" width="128" height="128">
</p>

<p align="center">
  <strong>macOS Sidecar 增强工具</strong><br>
  <sub>一键连接 · 远程控制 · 自动化集成</sub>
</p>

<p align="center">
  <a href="#-功能特性">功能特性</a> •
  <a href="#-安装">安装</a> •
  <a href="#-快速开始">快速开始</a> •
  <a href="#-使用指南">使用指南</a> •
  <a href="#-api-文档">API 文档</a> •
  <a href="#-mcp-集成">MCP 集成</a> •
  <a href="#-常见问题">常见问题</a>
</p>

<p align="center">
  <a href="https://github.com/yi-nology/sidecarOneStep/releases">
    <img src="https://img.shields.io/github/v/release/yi-nology/sidecarOneStep?style=flat-square" alt="Release">
  </a>
  <a href="https://github.com/yi-nology/sidecarOneStep/blob/master/LICENSE">
    <img src="https://img.shields.io/github/license/yi-nology/sidecarOneStep?style=flat-square" alt="License">
  </a>
  <a href="https://github.com/yi-nology/sidecarOneStep/stargazers">
    <img src="https://img.shields.io/github/stars/yi-nology/sidecarOneStep?style=flat-square" alt="Stars">
  </a>
  <img src="https://img.shields.io/badge/platform-macOS%2011.0%2B-lightgrey?style=flat-square" alt="Platform">
</p>

---

## 🎯 为什么选择 SidecarOneStep？

macOS 原生的**随航（Sidecar）**功能非常棒，可以让你把 iPad 作为 Mac 的第二块显示屏使用。但是：

| 痛点 | SidecarOneStep 的解决方案 |
|------|---------------------------|
| 🔍 **连接入口太深** - 需要多次点击系统设置 | 🚀 **一键连接** - 菜单栏直接管理 |
| 📶 **无线不稳定** - 经常断连、延迟高 | 🔌 **强制有线** - 稳定低延迟 |
| 🛌 **无法远程控制** - 必须在电脑前操作 | 📱 **Web 控制台** - 手机远程管理 |
| ⚙️ **无法自动化** - 每次都要手动点击 | 🛠️ **REST API** - 集成到工作流 |
| 🤖 **无法用 AI 管理** - 无法智能控制 | 🧠 **MCP 集成** - AI 助手直接管理 |

---

## ✨ 功能特性

### 🚀 极速连接
常驻菜单栏，一键连接/断开 iPad，告别繁琐的系统设置步骤。

**特性：**
- 实时显示可用设备列表
- 设备状态一目了然（已连接/未连接/不可用）
- 单击即可切换连接状态
- 支持多台 iPad 管理

### 📱 手机遥控（Web 控制台）
内置 Web 服务器，手机扫码即可远程控制 Mac 的随航连接状态。

**使用场景：**
- 🛌 躺在床上想切换 iPad 连接，但不想起身
- 🛋️ 在沙发上远程控制工作站的随航
- 🏠 在家中任意位置管理 Mac 设备

**特性：**
- 二维码扫码即用
- 局域网内任意设备访问
- 响应式界面，适配手机/平板
- 无需安装额外 App

### 🔌 有线稳定模式
支持强制有线连接模式，杜绝无线干扰。

**优势：**
- ⚡ **更低延迟** - USB 直连，响应更快
- 🔒 **更稳定** - 不受 WiFi 信号影响
- 🔋 **边充边用** - 连接同时为 iPad 充电
- 🎨 **适合创作** - 图形/视频/设计工作首选

### 🛠️ 自动化集成
提供完整 REST API，轻松集成到各种自动化工具。

**支持的集成方式：**
- **快捷指令（Shortcuts）** - iOS/macOS 原生自动化
- **Raycast** - macOS 效率工具
- **Alfred** - 经典 Mac 效率工具
- **Keyboard Maestro** - 宏自动化
- **自定义脚本** - Bash/Python/AppleScript

### 🤖 AI 助手集成（MCP）
内置 MCP 服务器，让 AI 助手直接管理随航连接。

**支持的 AI 助手：**
- **Claude Desktop** - Anthropic 官方客户端
- **Cursor** - AI 编程助手
- **OpenClaw** - 开源 AI 助手
- **OpenCode** - AI 代码助手
- **任何支持 MCP 的客户端**

**使用场景：**
- 💬 自然语言控制："连接我的 iPad"
- 🤖 AI 自动化："每天 9 点自动连接"
- 🔗 工作流集成：在 AI 对话中管理设备

**快速开始：**
```bash
# 查看预设配置
ls mcp-clients/
# claude_desktop.json  cursor.json  openclaw.json  opencode.json
```

👉 详细配置请查看 [MCP 集成](#-mcp-集成) 章节

---

## 📥 安装

### 系统要求

| 项目 | 最低要求 |
|------|---------|
| **macOS** | 11.0 (Big Sur) 或更高版本 |
| **Mac** | 支持 Sidecar 的 Mac（2016年及之后） |
| **iPad** | iPadOS 13.0 或更高版本 |
| **iPad** | 支持 Sidecar 的 iPad（2018年及之后） |

<details>
<summary>📋 Sidecar 支持设备列表</summary>

**支持的 Mac：**
- MacBook Pro (2016 及之后)
- MacBook Air (2018 及之后)
- MacBook (2016 及之后)
- iMac (2017 及之后)
- iMac Pro (2017 及之后)
- Mac mini (2018 及之后)
- Mac Pro (2019 及之后)

**支持的 iPad：**
- iPad Pro (所有型号)
- iPad (第 6 代及之后)
- iPad Air (第 3 代及之后)
- iPad mini (第 5 代及之后)
</details>

### 下载安装

#### 方式 1：GitHub Releases（推荐）
1. 前往 [Releases](https://github.com/yi-nology/sidecarOneStep/releases) 页面
2. 下载最新版本的 `.dmg` 文件
3. 打开 DMG，拖拽到 Applications 文件夹
4. 首次运行时，如遇安全提示：
   - 打开"系统偏好设置" → "安全性与隐私"
   - 点击"仍要打开"或"允许"

#### 方式 2：从源码构建
```bash
# 克隆仓库
git clone https://github.com/yi-nology/sidecarOneStep.git
cd sidecarOneStep

# 打开 Xcode 项目
open SidecarOneStep.xcodeproj

# 在 Xcode 中构建并运行 (Cmd+R)
```

---

## 🚀 快速开始

### 1️⃣ 首次启动
1. 打开 SidecarOneStep
2. 系统会请求辅助功能权限（用于模拟点击）
3. 点击"允许"
4. 菜单栏会出现图标

### 2️⃣ 连接 iPad
1. 点击菜单栏图标
2. 查看可用设备列表
3. 点击想连接的 iPad
4. 等待连接成功提示

### 3️⃣ 启用 Web 控制台（可选）
1. 点击菜单栏图标
2. 选择"偏好设置"
3. 勾选"启动时自动启动 Web 服务"
4. 使用手机扫描二维码

---

## 📖 使用指南

### 菜单栏管理

点击菜单栏图标后，你会看到：

```
┌─────────────────────────────┐
│ 📱 可用设备                  │
├─────────────────────────────┤
│ 🟢 iPad Pro 11  [已连接]     │
│ ⚪ iPad Air     [点击连接]   │
│ ⚫ iPad mini    [不可用]     │
├─────────────────────────────┤
│ ⚙️ 偏好设置                  │
│ 🌐 启动 Web 服务             │
│ ❌ 退出                      │
└─────────────────────────────┘
```

**状态说明：**
- 🟢 **绿色** - 已连接
- ⚪ **灰色** - 可用但未连接
- ⚫ **灰色（置底）** - 不可用（不在同一网络/未配对）

### Web 控制台

#### 启动服务
1. 点击菜单栏图标
2. 选择"启动 Web 服务"
3. 服务将在 `http://<你的IP>:8080` 启动

#### 手机访问
**方式 1：扫码**
- 点击菜单栏图标
- 扫描显示的二维码

**方式 2：手动输入**
- 在手机浏览器输入：`http://192.168.x.x:8080`

#### 功能列表
- 📋 查看设备列表
- 🔗 连接/断开设备
- 📊 查看连接状态
- ⚙️ 修改设置

### 强制有线模式

#### 为什么使用有线模式？
- **稳定性** - 避免 WiFi 干扰导致断连
- **低延迟** - USB 直连，响应更快
- **充电** - 使用同时为 iPad 充电
- **画质** - 更稳定的图像传输

#### 如何启用？
1. 点击菜单栏图标
2. 选择"偏好设置"
3. 勾选"强制有线连接"
4. 使用 USB 数据线连接 iPad

#### 注意事项
- 确保使用**数据线**而非仅充电线
- iPad 会在"信任此电脑"时弹出提示，点击"信任"
- 如连接失败，尝试重新插拔或重启 Mac

### 自动化示例

#### 快捷指令（Shortcuts）

**创建快捷指令：**
1. 打开"快捷指令" App
2. 创建新快捷指令
3. 添加"获取 URL 内容"动作
4. 输入 URL：`http://localhost:8080/api/connect?device=iPad-Pro-11`

**常用动作：**
```
# 连接设备
GET http://localhost:8080/api/connect?device=iPad-Pro-11

# 断开连接
GET http://localhost:8080/api/disconnect

# 查询状态
GET http://localhost:8080/api/status

# 获取设备列表
GET http://localhost:8080/api/devices
```

#### Raycast

**创建 Script Command：**

1. 创建脚本文件 `sidecar-connect.sh`：
```bash
#!/bin/bash
# @raycast.schemaVersion 1
# @raycast.title Sidecar Connect
# @raycast.mode silent

ACTION="${1:-status}"
API_URL="http://localhost:8080/api"

case $ACTION in
  connect)
    curl -s "$API_URL/connect?device=iPad-Pro-11"
    echo "Sidecar connected!"
    ;;
  disconnect)
    curl -s "$API_URL/disconnect"
    echo "Sidecar disconnected!"
    ;;
  status)
    curl -s "$API_URL/status"
    ;;
  *)
    echo "Usage: sidecar-connect.sh [connect|disconnect|status]"
    ;;
esac
```

2. 添加到 Raycast Script Commands 目录
3. 在 Raycast 中搜索并运行

#### Alfred Workflow

**创建 Workflow：**
1. 新建 Workflow
2. 添加 "Run Script" 动作
3. 输入脚本：

```bash
curl -X POST "http://localhost:8080/api/connect" \
  -H "Content-Type: application/json" \
  -d '{"device_id": "iPad-Pro-11"}'
```

#### AppleScript 示例

```applescript
-- 连接 Sidecar
do shell script "curl -X POST http://localhost:8080/api/connect -d '{\"device_id\":\"iPad-Pro-11\"}'"

-- 断开 Sidecar
do shell script "curl -X POST http://localhost:8080/api/disconnect"
```

#### Python 示例

```python
import requests

API_URL = "http://localhost:8080/api"

def connect_sidecar(device_id="iPad-Pro-11"):
    """连接 Sidecar 设备"""
    response = requests.post(f"{API_URL}/connect", json={
        "device_id": device_id
    })
    return response.json()

def disconnect_sidecar():
    """断开 Sidecar 连接"""
    response = requests.post(f"{API_URL}/disconnect")
    return response.json()

def get_status():
    """获取连接状态"""
    response = requests.get(f"{API_URL}/status")
    return response.json()

# 使用示例
if __name__ == "__main__":
    # 连接
    print(connect_sidecar())
    
    # 查看状态
    print(get_status())
    
    # 断开
    print(disconnect_sidecar())
```

---

## 🔌 API 文档

### 基础信息

| 项目 | 值 |
|------|-----|
| **Base URL** | `http://localhost:8080/api` |
| **Content-Type** | `application/json` |
| **认证** | 无（仅限本机访问） |

### 端点列表

#### GET /api/status
获取当前随航连接状态

**请求：**
```http
GET /api/status
```

**响应：**
```json
{
  "success": true,
  "connected": true,
  "device": {
    "id": "iPad-Pro-11",
    "name": "iPad Pro 11",
    "model": "iPad Pro (11-inch) (3rd generation)",
    "connection_type": "wired",
    "connected_at": "2025-03-09T15:30:00Z"
  }
}
```

**状态码：**
- `200` - 成功
- `500` - 服务器错误

---

#### GET /api/devices
获取所有可用的 iPad 设备列表

**请求：**
```http
GET /api/devices
```

**响应：**
```json
{
  "success": true,
  "devices": [
    {
      "id": "iPad-Pro-11",
      "name": "iPad Pro 11",
      "model": "iPad Pro (11-inch) (3rd generation)",
      "available": true,
      "connection_type": "wired"
    },
    {
      "id": "iPad-Air",
      "name": "iPad Air",
      "model": "iPad Air (4th generation)",
      "available": true,
      "connection_type": "wireless"
    },
    {
      "id": "iPad-mini",
      "name": "iPad mini",
      "model": "iPad mini (6th generation)",
      "available": false,
      "reason": "Not on same network"
    }
  ],
  "count": 3
}
```

---

#### POST /api/connect
连接指定设备

**请求：**
```http
POST /api/connect
Content-Type: application/json

{
  "device_id": "iPad-Pro-11",
  "force_wired": true
}
```

**参数：**
| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `device_id` | string | 是 | 设备 ID（从 /api/devices 获取） |
| `force_wired` | boolean | 否 | 强制使用有线连接（默认 false） |

**响应（成功）：**
```json
{
  "success": true,
  "message": "Connected to iPad Pro 11",
  "device": {
    "id": "iPad-Pro-11",
    "name": "iPad Pro 11",
    "connection_type": "wired"
  }
}
```

**响应（失败）：**
```json
{
  "success": false,
  "error": "Device not available",
  "reason": "iPad mini is not on the same network"
}
```

**状态码：**
- `200` - 连接成功
- `400` - 参数错误
- `404` - 设备不存在
- `500` - 连接失败

---

#### POST /api/disconnect
断开当前连接

**请求：**
```http
POST /api/disconnect
```

**响应：**
```json
{
  "success": true,
  "message": "Disconnected from iPad Pro 11"
}
```

**状态码：**
- `200` - 断开成功
- `404` - 当前无连接
- `500` - 断开失败

---

#### GET /api/config
获取当前配置

**请求：**
```http
GET /api/config
```

**响应：**
```json
{
  "success": true,
  "config": {
    "web_server_enabled": true,
    "web_server_port": 8080,
    "force_wired_mode": false,
    "auto_connect_on_startup": false,
    "preferred_device": "iPad-Pro-11"
  }
}
```

---

#### PUT /api/config
更新配置

**请求：**
```http
PUT /api/config
Content-Type: application/json

{
  "force_wired_mode": true,
  "auto_connect_on_startup": true
}
```

**响应：**
```json
{
  "success": true,
  "message": "Configuration updated",
  "config": {
    "force_wired_mode": true,
    "auto_connect_on_startup": true
  }
}
```

---

### 错误响应格式

所有错误遵循统一格式：

```json
{
  "success": false,
  "error": "Error type",
  "reason": "Detailed error message",
  "timestamp": "2025-03-09T15:30:00Z"
}
```

---

## 🤖 MCP 集成

SidecarOneStep 内置 **MCP (Model Context Protocol)** 服务器，可以直接与 Claude Desktop、Cursor、OpenClaw 等 AI 助手集成，让 AI 帮你管理随航连接！

### 什么是 MCP？

[MCP](https://modelcontextprotocol.io/) 是一个开放协议，允许 AI 助手（如 Claude、GPT-4）直接调用外部工具。通过 SidecarOneStep 的 MCP 服务器，你可以：

- 💬 **用自然语言控制** - "连接我的 iPad"、"断开随航"
- 🤖 **AI 自动化管理** - 让 AI 根据场景自动连接/断开
- 🔗 **集成到工作流** - 在 AI 对话中无缝管理设备

### 快速开始

#### 1. 确认 SidecarOneStep 已安装
```bash
# 检查 MCP 命令是否可用
/Applications/SidecarOneStep.app/Contents/MacOS/SidecarOneStep mcp --help
```

#### 2. 选择你的 MCP 客户端

<details>
<summary><strong>Claude Desktop</strong></summary>

**配置步骤：**

1. 打开 Claude Desktop 配置文件：
   ```bash
   # macOS
   open -e ~/Library/Application\ Support/Claude/claude_desktop_config.json
   ```

2. 添加 SidecarOneStep MCP 服务器：
   ```json
   {
     "mcpServers": {
       "sidecar_onestep": {
         "command": "/Applications/SidecarOneStep.app/Contents/MacOS/SidecarOneStep",
         "args": ["mcp"]
       }
     }
   }
   ```

3. 重启 Claude Desktop

4. 在对话中询问：
   > "What Sidecar devices are available?"
   > "Connect to my iPad"

</details>

<details>
<summary><strong>Cursor</strong></summary>

**配置步骤：**

1. 打开 Cursor 设置（`Cmd + ,`）
2. 搜索 "MCP" 或 "Model Context Protocol"
3. 添加 MCP 服务器配置：
   ```json
   {
     "mcpServers": {
       "sidecar_onestep": {
         "command": "/Applications/SidecarOneStep.app/Contents/MacOS/SidecarOneStep",
         "args": ["mcp"]
       }
     }
   }
   ```

4. 重启 Cursor

</details>

<details>
<summary><strong>OpenClaw</strong></summary>

**配置步骤：**

1. 编辑 OpenClaw 配置文件：
   ```bash
   open -e ~/.openclaw/config.json
   ```

2. 添加 MCP 服务器：
   ```json
   {
     "mcpServers": {
       "sidecar_onestep": {
         "command": "/Applications/SidecarOneStep.app/Contents/MacOS/SidecarOneStep",
         "args": ["mcp"]
       }
     }
   }
   ```

3. 重启 OpenClaw Gateway：
   ```bash
   openclaw gateway restart
   ```

</details>

<details>
<summary><strong>OpenCode</strong></summary>

**配置步骤：**

1. 编辑 OpenCode MCP 配置：
   ```bash
   open -e ~/.config/opencode/mcp_config.json
   ```

2. 添加服务器配置：
   ```json
   {
     "mcpServers": {
       "sidecar_onestep": {
         "command": "/Applications/SidecarOneStep.app/Contents/MacOS/SidecarOneStep",
         "args": ["mcp"]
       }
     }
   }
   ```

3. 重启 OpenCode

</details>

<details>
<summary><strong>自定义集成</strong></summary>

**使用任意 MCP 客户端：**

SidecarOneStep 的 MCP 服务器通过 `stdio` 通信，可以集成到任何支持 MCP 的客户端：

```bash
# 直接运行 MCP 服务器（用于调试）
/Applications/SidecarOneStep.app/Contents/MacOS/SidecarOneStep mcp

# 或使用调试构建
~/Library/Developer/Xcode/DerivedData/SidecarOneStep-xxx/Build/Products/Debug/SidecarOneStep mcp
```

**Node.js 示例：**
```javascript
import { Client } from "@modelcontextprotocol/sdk/client/index.js";
import { StdioClientTransport } from "@modelcontextprotocol/sdk/client/stdio.js";

const transport = new StdioClientTransport({
  command: "/Applications/SidecarOneStep.app/Contents/MacOS/SidecarOneStep",
  args: ["mcp"]
});

const client = new Client({ name: "sidecar-client", version: "1.0.0" }, {
  capabilities: {}
});

await client.connect(transport);

// 列出可用工具
const tools = await client.listTools();
console.log(tools);

// 调用工具
const result = await client.callTool({
  name: "connect_sidecar",
  arguments: { device_id: "iPad-Pro-11" }
});
```

</details>

### MCP 工具列表

SidecarOneStep 提供以下 MCP 工具：

| 工具名称 | 功能 | 参数 |
|---------|------|------|
| `list_devices` | 列出可用的 iPad 设备 | 无 |
| `connect_sidecar` | 连接到指定设备 | `device_id`, `force_wired` (可选) |
| `disconnect_sidecar` | 断开当前连接 | 无 |
| `get_status` | 获取连接状态 | 无 |
| `get_config` | 获取当前配置 | 无 |
| `set_config` | 更新配置 | 配置对象 |

### 使用示例

#### 与 Claude 对话示例

```
用户: What Sidecar devices do I have?

Claude: [调用 list_devices]
You have 2 available devices:
- iPad Pro 11 (wired connection available)
- iPad Air (wireless connection available)

用户: Connect to iPad Pro 11 with wired mode

Claude: [调用 connect_sidecar]
✅ Connected to iPad Pro 11 via wired connection.
Your iPad is now ready to use as a second display.

用户: What's the current connection status?

Claude: [调用 get_status]
Currently connected to:
- Device: iPad Pro 11
- Connection: Wired (USB)
- Connected since: 2025-03-09 23:50:00
```

#### 自动化场景示例

**场景 1：工作日开始时自动连接**
```
用户: Every weekday at 9 AM, if I'm at my desk, connect to my iPad

Claude: I'll set up an automation that:
1. Checks your location at 9 AM on weekdays
2. If you're at your desk location
3. Connects to iPad Pro 11 in wired mode
4. Sends you a notification
```

**场景 2：会议前自动准备**
```
用户: 5 minutes before my meetings, connect to iPad for note-taking

Claude: [集成日历 API + SidecarOneStep MCP]
I'll monitor your calendar and:
1. Detect upcoming meetings
2. 5 minutes before start, connect to iPad
3. Open your note-taking app on iPad
```

### 调试 MCP

**查看 MCP 日志：**
```bash
# 启用详细日志
export SIDECARONESTEP_MCP_DEBUG=1
/Applications/SidecarOneStep.app/Contents/MacOS/SidecarOneStep mcp
```

**测试 MCP 工具：**
```bash
# 使用 MCP Inspector
npx @modelcontextprotocol/inspector \
  /Applications/SidecarOneStep.app/Contents/MacOS/SidecarOneStep mcp
```

### 预设配置文件

项目提供了预配置的 MCP 客户端配置文件：

```bash
# 查看所有预设配置
ls /opt/project/sidecarOneStep/mcp-clients/

# 输出：
# - claude_desktop.json
# - cursor.json
# - openclaw.json
# - opencode.json
```

直接复制到你的客户端配置目录即可使用。

### 安全说明

- ✅ MCP 服务器仅监听本地 `stdio`，不开放网络端口
- ✅ 所有操作都在本机执行
- ✅ 不会向外部服务发送数据
- ⚠️ 确保只在受信任的 AI 客户端中使用

---

## ❓ 常见问题

<details>
<summary><strong>Q: 为什么无法连接 iPad？</strong></summary>

**A:** 请按照以下步骤排查：

1. **检查 iCloud 账户**
   - iPad 和 Mac 必须登录同一个 iCloud 账户
   - 使用双重认证的账户需确认已验证

2. **检查系统设置**
   - 打开"系统偏好设置" → "随航"
   - 确认 iPad 出现在设备列表中

3. **检查设备兼容性**
   - Mac: 2016 年及之后
   - iPad: 2018 年及之后
   - [查看完整支持列表](#系统要求)

4. **检查网络连接**
   - 无线模式：确保在同一 WiFi 网络
   - 有线模式：确保使用 USB 数据线

5. **重启相关服务**
   - 重启 Mac
   - 重启 iPad
   - 重新登录 iCloud
</details>

<details>
<summary><strong>Q: 有线模式有什么优势？</strong></summary>

**A:** 有线模式提供：

| 特性 | 有线模式 | 无线模式 |
|------|---------|---------|
| **延迟** | ⚡ 极低 (~5ms) | 较高 (~20-50ms) |
| **稳定性** | 🔒 非常稳定 | 受 WiFi 影响 |
| **充电** | ✅ 同时充电 | ❌ 不充电 |
| **画质** | 🎨 更稳定 | 可能有波动 |
| **便携性** | ❌ 需要线缆 | ✅ 无需线缆 |

**推荐使用场景：**
- ✅ 图形设计、视频剪辑
- ✅ 编程开发（需要第二屏幕）
- ✅ 长时间会议/演示
- ✅ 对延迟敏感的应用

**不推荐场景：**
- ❌ 临时快速查看
- ❌ 需要频繁移动
</details>

<details>
<summary><strong>Q: Web 控制台安全吗？</strong></summary>

**A:** 安全性说明：

**当前安全措施：**
- ✅ 仅监听局域网（127.0.0.1 / 192.168.x.x）
- ✅ 不对外开放端口
- ✅ 无公网访问

**建议：**
- ⚠️ 仅在受信任的 WiFi 网络使用
- ⚠️ 避免在公共 WiFi 启用
- ⚠️ 如需远程访问，使用 VPN

**未来计划：**
- 🔐 密码保护
- 🔐 HTTPS 支持
- 🔐 Token 认证
- 🔐 访问日志
</details>

<details>
<summary><strong>Q: 提示"需要辅助功能权限"怎么办？</strong></summary>

**A:** SidecarOneStep 需要辅助功能权限来模拟系统点击。

**授权步骤：**
1. 打开"系统偏好设置" → "安全性与隐私" → "隐私"
2. 选择左侧"辅助功能"
3. 点击左下角🔒解锁（需要输入密码）
4. 勾选 SidecarOneStep
5. 重启 SidecarOneStep

**如果仍无法授权：**
```bash
# 重置权限数据库
tccutil reset Accessibility

# 然后重新打开 SidecarOneStep
```
</details>

<details>
<summary><strong>Q: 可以同时连接多台 iPad 吗？</strong></summary>

**A:** macOS Sidecar 原生**不支持**同时连接多台 iPad 作为扩展屏。

**但是你可以：**
- 使用 SidecarOneStep 快速切换不同 iPad
- 在菜单栏中一键断开当前设备并连接另一台
- 通过 API 实现自动切换

**替代方案：**
- 使用 Luna Display（支持多台 iPad）
- 使用 Duet Display（支持多台设备）
</details>

<details>
<summary><strong>Q: API 端口可以修改吗？</strong></summary>

**A:** 可以！

**方式 1：GUI 设置**
1. 点击菜单栏图标
2. 选择"偏好设置"
3. 修改"Web 服务端口"

**方式 2：API 修改**
```bash
curl -X PUT http://localhost:8080/api/config \
  -H "Content-Type: application/json" \
  -d '{"web_server_port": 9090}'
```

**方式 3：配置文件**
编辑 `~/.sidecaronestep/config.json`：
```json
{
  "web_server_port": 9090
}
```
</details>

---

## 🗺️ 路线图

### v1.0（当前版本）
- [x] 菜单栏快速连接
- [x] Web 控制台
- [x] REST API
- [x] 强制有线模式

### v1.1（计划中）
- [ ] 密码保护 Web 控制台
- [ ] HTTPS 支持
- [ ] 连接状态通知
- [ ] 自定义快捷键

### v1.2（未来）
- [ ] Apple Watch 控制
- [ ] iOS 配套 App
- [ ] 连接历史记录
- [ ] 自动连接规则

### v2.0（长期目标）
- [ ] 多显示器管理
- [ ] 跨设备同步
- [ ] 插件系统

---

## 🤝 贡献

欢迎贡献代码、报告 Bug 或提出新功能建议！

### 如何贡献

1. **报告 Bug**
   - 在 [Issues](https://github.com/yi-nology/sidecarOneStep/issues) 中搜索是否已存在
   - 如果不存在，创建新 Issue
   - 提供详细的复现步骤和系统信息

2. **提交代码**
   ```bash
   # Fork 仓库
   git clone https://github.com/your-username/sidecarOneStep.git
   
   # 创建分支
   git checkout -b feature/your-feature
   
   # 提交更改
   git commit -am 'Add some feature'
   
   # 推送到分支
   git push origin feature/your-feature
   
   # 创建 Pull Request
   ```

3. **翻译**
   - 帮助翻译文档到其他语言
   - 改进现有翻译

### 开发环境设置

```bash
# 克隆仓库
git clone https://github.com/yi-nology/sidecarOneStep.git
cd sidecarOneStep

# 安装依赖（如有）
# make install

# 运行测试（如有）
# make test

# 构建项目
# make build
```

### 代码规范
- 遵循 Swift 代码规范
- 添加必要的注释
- 更新相关文档

---

## 📄 License

本软件为免费软件，采用 [MIT License](LICENSE) 开源协议。

```
Copyright © 2025 MurphyYi. All rights reserved.

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.
```

---

## 📞 联系方式

- 🏠 **官网**: [https://sidecaronestep.app.murphyyi.com/](https://sidecaronestep.app.murphyyi.com/)
- 🐙 **GitHub**: [yi-nology/sidecarOneStep](https://github.com/yi-nology/sidecarOneStep)
- 📧 **Email**: [your-email@example.com]
- 🐦 **Twitter**: [@MurphyYi]

---

## 🙏 致谢

感谢以下项目和资源的启发：
- [macOS Sidecar](https://support.apple.com/zh-cn/guide/mac-help/mchl9c25366e/mac) - Apple 官方随航功能
- [Raycast](https://www.raycast.com/) - 效率工具灵感来源
- [Alfred](https://www.alfredapp.com/) - 工作流自动化参考

---

<p align="center">
  <strong>如果这个项目对你有帮助，欢迎 ⭐️ Star 支持！</strong>
</p>

<p align="center">
  Made with ❤️ by <a href="https://github.com/yi-nology">MurphyYi</a>
</p>
