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
  <a href="https://github.com/yi-nology/sidecarOneStep/blob/main/LICENSE">
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

> **前置条件**
> 1. 偏好设置里开启「启动时自动启动 Web 服务」，或从菜单栏手动「启动 Web 服务」
> 2. 记下实际端口（默认 `8080`）
> 3. 设备名先用 `GET /devices` 查出来，**脚本里不要硬编码**（设备名含空格和中文，变了就失效）

> 💡 **SidecarOneStep 本身还没有全局快捷键**（自定义快捷键排在 v1.1 路线图里）。
> 下面所有方案都是用 macOS 现成的自动化工具当「触发器」，再通过 REST API 驱动 App 干活。

#### 快捷指令（Shortcuts）

用 macOS 自带的「快捷指令」App：

1. 新建快捷指令，命名如「连接随航」
2. 添加「获取 URL 内容」动作
3. 方法选 **POST**（不是 GET）
4. URL：`http://localhost:8080/connect`
5. 点「添加请求头」：`Content-Type` = `application/json`
6. 请求体选「JSON」：`{"name":"iPad Pro","wired":true}`
7. 保存后点 ⌘⌥ 打开「快捷指令」App →「键盘快捷键」→ 找到这个快捷指令 → 分配组合键

断开同理：URL 换成 `/disconnect`，请求体 `{"name":"iPad Pro"}`。

#### Raycast

创建 Script Command，脚本存到 `~/Library/Application Support/Raycast/Scripts/sidecar.sh`：

```bash
#!/bin/bash
# @raycast.schemaVersion 1
# @raycast.title Sidecar
# @raycast.description 连接 / 断开 / 切换 iPad 随航
# @raycast.mode silent
# @raycast.argument1 { "type": "text", "placeholder": "connect | disconnect | toggle | devices", "optional": false }
# @raycast.argument2 { "type": "text", "placeholder": "设备名（留空 = 第一个可用设备）", "optional": true }
# @raycast.argument3 { "type": "text", "placeholder": "wired | wireless（留空 = 不强制）", "optional": true }

API="http://localhost:${SIDECAR_PORT:-8080}"
ACTION="$1"
NAME="$2"
MODE="$3"

case "$ACTION" in
  connect)    ENDPOINT="/connect";    METHOD="POST" ;;
  disconnect) ENDPOINT="/disconnect"; METHOD="POST" ;;
  toggle)     ENDPOINT="/toggle";     METHOD="POST" ;;
  devices)    ENDPOINT="/devices";    METHOD="GET" ;;
  *) echo "用法：connect | disconnect | toggle | devices"; exit 1 ;;
esac

# 名字留空 = 服务端自动挑第一个可用设备
BODY="{}"
if [ -n "$NAME" ]; then
  if [ "$ENDPOINT" = "/connect" ] && [ -n "$MODE" ]; then
    BODY="{\"name\":\"$NAME\",\"wired\":$([ "$MODE" = "wired" ] && echo true || echo false)}"
  else
    BODY="{\"name\":\"$NAME\"}"
  fi
fi

RESP=$(curl -s -X "$METHOD" "$API$ENDPOINT" -H "Content-Type: application/json" -d "$BODY")

# 统一按 code 判断成败（code == 0 才是成功）
if printf '%s' "$RESP" | grep -q '"code"[[:space:]]*:[[:space:]]*0'; then
  echo "$RESP"
else
  echo "失败：$RESP" >&2
  exit 1
fi
```

把文件设为可执行（`chmod +x`），然后在 Raycast 里搜「Sidecar」即可。

#### Alfred Workflow

**基础版：关键词 + 可选全局快捷键**

1. 新建 Workflow，命名如「Sidecar」
2. 从右侧拖入 **Run Script** 动作，脚本填：

```bash
#!/bin/bash
API="http://localhost:${SIDECAR_PORT:-8080}"
DEVICE="${1:-}"        # 留空 = 第一个可用设备
MODE="${2:-}"          # wired | wireless，留空 = 不强制

BODY="{}"
if [ -n "$DEVICE" ]; then
  if [ -n "$MODE" ]; then
    BODY="{\"name\":\"$DEVICE\",\"wired\":$([ "$MODE" = "wired" ] && echo true || echo false)}"
  else
    BODY="{\"name\":\"$DEVICE\"}"
  fi
fi

RESP=$(curl -s -X POST "$API/connect" \
  -H "Content-Type: application/json" \
  -d "$BODY")

if printf '%s' "$RESP" | grep -q '"code"[[:space:]]*:[[:space:]]*0'; then
  echo "$RESP"
else
  echo "连接失败：$RESP"
fi
```

3. 右键（或双击）Workflow 标题 → **Workflow Settings**
   - **Keyword**：填 `sidecar`（这就是「口令」：⌥⌘ 打开 Alfred → 输入 `sidecar` → 回车）
   - **Hotkey**：填 `⌥⌘S` 之类，就能用全局快捷键直接触发，不用打字
   - 若你的 Alfred 版本没有 Hotkey 字段，改用下面的 Raycast 或 Keyboard Maestro 方案
4. 断开的话再建一个 Run Script 动作，把 URL 换成 `/disconnect` 即可

**进阶版：用 Script Filter 选设备**

把上面的 Run Script 换成 **Script Filter**（`type: "afzf"`，Keyword 设为 `sidecar`），
再用 **Run Script**（`type: "bash"`，`withVariables: true`）执行连接：

```bash
# 1) Script Filter（type: afzf，Keyword 设为 sidecar）——列出设备供 Alfred 搜索
#    afzf 要求输出 JSON 数组：arg 会作为 {query} 传给下一步
API="http://localhost:${SIDECAR_PORT:-8080}"
curl -s "$API/devices" | python3 -c '
import json, sys
try:
    names = json.load(sys.stdin)["data"]["devices"]
except Exception:
    names = []
print(json.dumps(
    [{"arg": n, "title": n, "subtitle": "Sidecar 设备", "valid": True} for n in names],
    ensure_ascii=False))
'
```

```bash
# 2) Run Script（bash, withVariables: true）——连接选中的设备
DEVICE="{query}"
BODY="{}"
[ -n "$DEVICE" ] && BODY="{\"name\":\"$DEVICE\"}"
curl -s -X POST "http://localhost:${SIDECAR_PORT:-8080}/connect" \
  -H "Content-Type: application/json" \
  -d "$BODY"
```

#### Automator / AppleScript

**Automator**（拿全局快捷键最省事的办法）：

1. 新建 Automator 动作 → 选「快速操作」或「应用程序」
2. 拖入 **Run Shell Script**，填：

```bash
curl -s -X POST "http://localhost:8080/connect" \
  -H "Content-Type: application/json" \
  -d '{"name":"iPad Pro"}'
```

3. 保存成 `连接随航.workflow`
4. 打开 **系统设置 → 键盘快捷键 → App 快捷键 → Automator** → 勾选「连接随航」→ 设一个组合键

这样就是一个真正的全局快捷键，任意 App 下都能唤起。

**AppleScript**：

```applescript
-- 连接 Sidecar
do shell script "curl -s -X POST http://localhost:8080/connect -H 'Content-Type: application/json' -d '{\"name\":\"iPad Pro\"}'"

-- 断开 Sidecar
do shell script "curl -s -X POST http://localhost:8080/disconnect -H 'Content-Type: application/json' -d '{}'"

-- 列出设备
do shell script "curl -s http://localhost:8080/devices"
```

#### Keyboard Maestro

1. 新建宏 → 触发器选 **快捷键**，指定组合键
2. 动作选 **执行 shell 脚本**：

```bash
curl -s -X POST "http://localhost:8080/connect" \
  -H "Content-Type: application/json" \
  -d '{"name":"iPad Pro"}'
```

Keyboard Maestro 还支持用 **Type/Text Trigger** 监听打字内容，适合做「口令」。

#### Python 示例

> 需要 `pip3 install requests`

```python
import os
import requests

API = f"http://localhost:{os.environ.get('SIDECAR_PORT', '8080')}"
HEADERS = {"Content-Type": "application/json"}
TIMEOUT = 30


def list_devices():
    """列出可用设备名"""
    r = requests.get(f"{API}/devices", headers=HEADERS, timeout=10)
    return r.json()["data"]["devices"]


def connect(name="", wired=False):
    """连接设备。name 留空 = 第一个可用设备"""
    r = requests.post(f"{API}/connect", headers=HEADERS,
                      json={"name": name, "wired": wired}, timeout=TIMEOUT)
    return r.json()


def disconnect(name=""):
    """断开设备"""
    r = requests.post(f"{API}/disconnect", headers=HEADERS,
                      json={"name": name}, timeout=TIMEOUT)
    return r.json()


def toggle(name=""):
    """切换连接状态"""
    r = requests.post(f"{API}/toggle", headers=HEADERS,
                      json={"name": name}, timeout=TIMEOUT)
    return r.json()


if __name__ == "__main__":
    print(list_devices())
    print(connect("iPad Pro", wired=True))
    print(toggle("iPad Pro"))
```

#### 🔤 口令触发（关键词 / 语音）

不想用快捷键，也可以用「口令」——打几个字（或说一句话）就触发：

| 工具 | 口令形式 | 配置位置 |
|------|---------|---------|
| **Alfred** | 敲 `sidecar` 回车 | Workflow Settings → Keyword |
| **Raycast** | 打开 Raycast 敲 `sidecar` | Script Command 的 `@raycast.title` |
| **快捷指令** | 用「听写」说出触发词 | 自动化 → 运行快捷指令 → 听写文本是「随航」 |
| **Keyboard Maestro** | 敲入关键词 | 触发器 → Type/Text Trigger |
| **Hammerspoon** | 敲入/说出关键词 | `hs.textExpander` / `hs.hotkey` |

Hammerspoon 示例（⌥⌘S 连接 + 关键词「随航」触发）：

```lua
-- ~/.hammerspoon/init.lua
local function sidecar()
  hs.osascript([[
    do shell script "curl -s -X POST http://localhost:8080/connect -H 'Content-Type: application/json' -d '{}'"
  ]])
end

hs.hotkey.bind({"cmd", "alt"}, "S", sidecar)

hs.textExpander.new("随航", sidecar)
hs.textExpander:bindHotkeys({ {"cmd", "alt"}, "E" })
```

> `hs.textExpander` 会把命中的关键词替换成对应文本；若要**执行**动作，用 `hs.audiotext`（监听听写结果）或 `hs.eventtap`（监听按键）触发上面的函数。

---

## 🔌 API 文档

### 基础信息

| 项目 | 值 |
|------|-----|
| **Base URL** | `http://localhost:<端口>`（默认 `8080`，可在偏好设置中修改） |
| **Content-Type** | `application/json`（POST 请求必须带） |
| **认证** | 默认关闭；开启后需带 `X-API-KEY` 请求头 |
| **交互式文档** | `http://localhost:<端口>/docs`（需在偏好设置中开启「允许访问 API 文档」） |

> ⚠️ **路径没有 `/api` 前缀。** 真实路径是 `/connect`、`/devices`；
> `http://localhost:8080/api/connect` 会返回 404。

### 端点速查

| 方法 | 路径 | 说明 | 请求体 |
|------|------|------|--------|
| `GET` | `/devices` | 列出可用设备 | — |
| `POST` | `/connect` | 连接设备 | `{ "name": "iPad Pro", "wired": true }` |
| `POST` | `/disconnect` | 断开设备 | `{ "name": "iPad Pro" }` |
| `POST` | `/toggle` | 切换连接状态 | `{ "name": "iPad Pro" }` |
| `GET` | `/virtual_display/status` | 虚拟显示器状态 | — |
| `GET` | `/virtual_display/sizes` | 可用尺寸预设列表 | — |
| `POST` | `/virtual_display/size` | 设置尺寸预设 | `{ "definition_id": 10 }` |
| `POST` | `/virtual_display/enable` | 启用虚拟显示器 | — |
| `POST` | `/virtual_display/disable` | 关闭虚拟显示器 | — |

### 统一响应格式

所有响应都是同一个信封结构：

```json
{
  "code": 0,
  "message": "success",
  "data": { }
}
```

| 字段 | 说明 |
|------|------|
| `code` | `0` 表示成功，非 `0` 表示错误 |
| `message` | 可读的结果描述 |
| `data` | 业务数据；出错时为 `null` |

> ⚠️ 判断成功**请看 `code == 0`**，不要只看 HTTP 状态码，也不要找 `success` 字段——本 API 不返回 `success`。

---

#### GET /devices
获取所有可用设备

**请求：**
```http
GET /devices
```

**响应：**
```json
{
  "code": 0,
  "message": "success",
  "data": {
    "devices": ["iPad Pro", "iPad Air"]
  }
}
```

`devices` 是**设备名字符串数组**（不是对象数组）。这个值就是后续 `/connect` 等接口的 `name` 参数取值。

---

#### POST /connect
连接指定设备

**请求：**
```http
POST /connect
Content-Type: application/json

{
  "name": "iPad Pro",
  "wired": true
}
```

**参数：**
| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `name` | string | 否 | 设备名（从 `/devices` 获取）。留空则自动选择第一个可用设备 |
| `wired` | boolean | 否 | 是否强制有线连接，默认 `false`（无线） |

**响应（成功）：**
```json
{
  "code": 0,
  "message": "success",
  "data": {
    "device_name": "iPad Pro",
    "status": "connected"
  }
}
```

**响应（失败）：**
```json
{
  "code": 1,
  "message": "No reachable Sidecar devices detected",
  "data": null
}
```

> 设备名必须与 `/devices` 返回的字符串**完全一致**（含空格与中文）。
> 不确定时先调 `/devices`，把结果原样传回。

---

#### POST /disconnect
断开连接

**请求：**
```http
POST /disconnect
Content-Type: application/json

{
  "name": "iPad Pro"
}
```

**参数：**
| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `name` | string | 否 | 设备名。留空则断开当前连接 |

**响应：**
```json
{
  "code": 0,
  "message": "success",
  "data": {
    "device_name": "iPad Pro",
    "status": "disconnected"
  }
}
```

---

#### POST /toggle
切换连接状态（已连接则断开，未连接则连接）

**请求：**
```http
POST /toggle
Content-Type: application/json

{
  "name": "iPad Pro"
}
```

**参数：**
| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| `name` | string | 否 | 设备名。留空则作用于第一个可用设备 |

**响应：**
```json
{
  "code": 0,
  "message": "success",
  "data": {
    "result": "Successfully connected to 'iPad Pro'."
  }
}
```

> 💡 做「一键开关」时用 `/toggle` 比 `/connect` + `/disconnect` 更省事。

---

#### 虚拟显示器

| 方法 | 路径 | 说明 |
|------|------|------|
| `GET` | `/virtual_display/status` | 返回 `{ "enabled": bool, "active": bool, "definition_id": int }` |
| `GET` | `/virtual_display/sizes` | 返回尺寸预设数组 `{ "id": int, "description": "..." }` |
| `POST` | `/virtual_display/size` | 请求体 `{ "definition_id": int }`，设置当前尺寸预设 |
| `POST` | `/virtual_display/enable` | 启用虚拟显示器（用当前尺寸预设） |
| `POST` | `/virtual_display/disable` | 关闭虚拟显示器 |

尺寸预设 ID（如 `10` = 16:9、`400` = iPad Pro 11）见 [MCP-API.md](mcp-clients/MCP-API.md#12-list_virtual_display_sizes)。

---

### 认证

在偏好设置中开启「启用认证」后，所有请求都要带 API Key：

```bash
curl -X POST "http://localhost:8080/connect" \
  -H "Content-Type: application/json" \
  -H "X-API-KEY: <你的 API Key>" \
  -d '{"name":"iPad Pro"}'
```

---

### 端口

端口在**偏好设置 → Web 服务端口**里修改（默认 `8080`），**改完需要重启服务**才生效。

脚本里如果不想把端口写死，可以先读一次偏好设置，或用环境变量：

```bash
PORT="${SIDECAR_PORT:-8080}"
curl -s "http://localhost:${PORT}/devices"
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

// 调用工具（异步连接，避免阻塞）
const result = await client.callTool({
  name: "connect_device_async",
  arguments: { device_name: "iPad Pro", wired: false }
});
```

</details>

### MCP 工具列表

SidecarOneStep 提供以下 MCP 工具（完整参数与返回示例见 [mcp-clients/MCP-API.md](mcp-clients/MCP-API.md)）：

| 工具名称 | 功能 | 参数 |
|---------|------|------|
| `list_devices` | 列出可用的 iPad 设备 | 无 |
| `connect_device` | 同步连接设备（**可能阻塞约 15s**） | `device_name`, `wired` (可选) |
| `connect_device_async` | 异步连接，返回 `job_id`（**推荐**） | `device_name`, `wired` (可选) |
| `get_job_status` | 查询异步任务结果 | `job_id` |
| `cancel_job` | 取消等待中的任务 | `job_id` |
| `disconnect_device` | 断开设备 | `device_name` (可选) |
| `start_http_server` | 启动 HTTP 控制服务 | `port` (可选) |
| `stop_http_server` | 停止 HTTP 控制服务 | 无 |
| `get_status` | 获取 App 与连接状态 | 无 |
| `get_logs` | 读取最近的服务日志 | `limit` (可选) |
| `virtual_display_status` | 获取虚拟显示器状态 | 无 |
| `list_virtual_display_sizes` | 列出可用尺寸预设 | 无 |
| `set_virtual_display_size` | 设置尺寸预设 | `definition_id` |
| `enable_virtual_display` | 启用虚拟显示器 | 无 |
| `disable_virtual_display` | 关闭虚拟显示器 | 无 |

> ⚠️ MCP 工具的参数名是 `device_name` / `wired`，
> **和 REST API 的 `name` / `wired` 不一样**——REST 用 `name`，MCP 用 `device_name`。

### 使用示例

#### 与 Claude 对话示例

```
用户: What Sidecar devices do I have?

Claude: [调用 list_devices]
You have 2 available devices:
- iPad Pro 11 (wired connection available)
- iPad Air (wireless connection available)

用户: Connect to iPad Pro 11 with wired mode

Claude: [调用 connect_device_async → 拿到 job_id，再轮询 get_job_status]
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
ls mcp-clients/

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
- ✅ 默认仅本机访问（`127.0.0.1`）
- ✅ 可在偏好设置里开启 **「启用认证」**——之后所有请求都要带 `X-API-KEY` 请求头
- ✅ 「允许公网访问」默认关闭；开启后局域网内其他设备也能访问控制页
- ✅ 「允许访问 API 文档 (/docs)」默认关闭，需要时再单独开

**建议：**
- ⚠️ 开启「允许公网访问」务必同时打开「启用认证」并设置强 API Key
- ⚠️ 仅在受信任的 WiFi 网络使用
- ⚠️ 避免在公共 WiFi 启用
- ⚠️ 如需远程访问，优先使用 VPN

**未来计划：**
- 🔐 HTTPS 支持
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

**A:** 可以！在**偏好设置 → Web 服务端口**里改（默认 `8080`）。

> ⚠️ **改完需要重启服务**才生效（菜单栏 → 停止 Web 服务 → 重新启动）。

也可以用 MCP 工具在启动时指定端口：

```json
{"jsonrpc":"2.0","id":8,"method":"tools/call","params":{"name":"start_http_server","arguments":{"port":9090}}}
```

脚本里建议用环境变量，别把端口写死：

```bash
PORT="${SIDECAR_PORT:-8080}"
curl -s "http://localhost:${PORT}/devices"
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

- 🏠 **官网**: [https://sidecaronestep.app.murphyyi.com/](https://sidecaronestep.app.murphyyi.com/)（文档站建设中，当前以本文档与 `/docs` 为准）
- 📦 **下载**: [Releases](https://github.com/yi-nology/sidecarOneStep/releases)
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
