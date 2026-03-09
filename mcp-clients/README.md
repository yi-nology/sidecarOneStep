# MCP Client Configs

These are starter configs for popular MCP clients.

## Command
The MCP server is built into SidecarOneStep and starts with the `mcp` subcommand:

```
SidecarOneStep mcp
```

Update the `command` path in each config to the actual executable you want to run.

Examples:
- Debug build: `/Users/zhangyi/Library/Developer/Xcode/DerivedData/.../Build/Products/Debug/SidecarOneStep`
- Installed app: `/Applications/SidecarOneStep.app/Contents/MacOS/SidecarOneStep`

## Notes
- These configs use stdio.
- If your client requires a different schema, adjust the JSON accordingly.
