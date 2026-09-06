> [AiDoIt 首页](../../../README.md) / [帮助中心](../../README.md) / Windows 安装

# AiDoIt Windows v0.0.9 安装与升级

本文适用于 Windows 10/11 x64，介绍 `v0.0.9` 安装包选择、文件完整性校验、安装升级、首次启动和卸载恢复。

## 1. 选择下载文件

请从 [AiDoIt GitHub Releases](https://github.com/AiDoIt-Platform/AiDoIt/releases/latest) 下载文件。

| 文件 | 适用场景 | 下载 |
|---|---|---|
| `AiDoIt_0.0.9_x64-setup.exe` | 标准安装程序，推荐大多数用户使用 | [下载 Setup](https://github.com/AiDoIt-Platform/AiDoIt/releases/download/v0.0.9/AiDoIt_0.0.9_x64-setup.exe) |

若已安装旧版本，请完全退出 AiDoIt 和相关客户端，再使用 `v0.0.9` 的标准安装程序覆盖升级。

## 2. 校验文件完整性

Release 页面同时提供 [`windows-ota-SHA256SUMS.txt`](https://github.com/AiDoIt-Platform/AiDoIt/releases/download/v0.0.9/windows-ota-SHA256SUMS.txt)。在下载目录打开 PowerShell，运行：

```powershell
Get-FileHash .\AiDoIt_0.0.9_x64-setup.exe -Algorithm SHA256
```

将输出的 `Hash` 与 `windows-ota-SHA256SUMS.txt` 中同名文件的值比较。两者必须完全一致；不一致时请删除文件并重新从 GitHub Releases 下载。

如需一次校验全部已下载的 `0.0.9` 文件：

```powershell
Get-FileHash .\AiDoIt_0.0.9_x64* -Algorithm SHA256
```

本次正式发布的安装包 SHA-256 如下：

| 文件 | SHA-256 |
|---|---|
| `AiDoIt_0.0.9_x64-setup.exe` | `12c9122adac9180e4e20ddb45be7dca62dfbb991285f6ea2c3ed3ee7e2933102` |

## 3. 安装或升级

### 应用内 OTA 更新

Windows `v0.0.9` 已包含应用内更新能力。AiDoIt 可发现后续正式版本，也可在设置页面手动检查。发现更新后，应用会显示发布说明与下载进度，并使用内置公钥验证 updater 签名后再完成安装与重启。

如果当前版本没有应用内更新入口，或在线更新失败，请从 Releases 手动下载 `v0.0.9` 并按下方步骤覆盖安装。

### 标准安装程序

1. 完全退出 AiDoIt、Codex、ChatGPT、Claude 和 Claude Code。
2. 双击 `AiDoIt_0.0.9_x64-setup.exe`。
3. 按安装向导完成安装，然后从开始菜单启动 AiDoIt。
4. 首次启动后确认版本为 `0.0.9`，再检查已有 Provider 与路由状态。

## 4. Windows 安全提示

如果 Windows Defender SmartScreen 显示“Windows 已保护你的电脑”，请先核对下载来源和 SHA-256。确认文件来自本仓库且校验一致后，点击 **更多信息 → 仍要运行**。如果来源或校验不一致，请不要运行。

## 5. 首次使用

安装完成后，根据需要继续阅读：

- [接入 Codex（Windows）](../Codex/README.md)
- [接入 Claude（Windows）](../Claude/README.md)

建议先添加并验证 Provider，再选择模型和开启智能路由。关闭路由时，AiDoIt 会尝试恢复启用前保存的官方配置。

## 6. 常见升级问题

### 升级后没有看到新模型

完全退出对应的桌面端和 CLI，关闭后重新开启智能路由，再重新启动客户端。仍无模型时，重新检测 Provider 并保存模型列表。

### AiDoIt 没有检测到 Codex CLI 或 Claude Code CLI

先在新的 PowerShell 窗口中确认 `codex --version` 或 `claude --version` 可以运行，再重启 AiDoIt。若命令不存在，请先安装相应 CLI，并确认其目录已经加入用户 `PATH`。

### Provider 检测失败

检查 Base URL、API Key、网络连接以及 Provider 是否支持相应协议。不要在截图、Issue 或聊天记录中公开完整 API Key。

## 7. 卸载与恢复

卸载前先在 AiDoIt 中分别关闭 Codex 与 Claude 智能路由，确认官方配置已经恢复，然后完全退出相关应用。

- 标准安装版：在 **Windows 设置 → 应用 → 已安装的应用** 中卸载 AiDoIt。

如果卸载后客户端状态异常，重新安装 AiDoIt，关闭对应智能路由并执行恢复，再卸载一次；仍未解决时请在 [GitHub Issues](https://github.com/AiDoIt-Platform/AiDoIt/issues/new) 提交问题，并附上系统版本、AiDoIt 版本和错误信息。

## 8. 下一步

- [接入 Codex（Windows）](../Codex/README.md)
- [接入 Claude（Windows）](../Claude/README.md)
- [返回帮助中心](../../README.md)
