> [AiDoIt 首页](../../../README.md) / [帮助中心](../../README.md) / macOS / Codex

# AiDoIt 接入 Codex（macOS）

本文按照图片顺序说明 AiDoIt 在 macOS 上的安装、Provider 配置及 Codex 智能路由使用方法。

> 请仅使用可信来源提供的 Base URL 和 API Key。图中的 Provider 名称、模型及地址仅作为示例，请以自己的服务信息为准。

> [!NOTE]
> macOS 与 Windows 使用不同的安装包和发布节奏；Windows `v0.0.7` 安装包不能用于 macOS。请从 [GitHub Releases](https://github.com/AiDoIt-Platform/AiDoIt/releases) 获取适合 Mac 的版本。

完成路径：**安装并授权 → 新增 Provider → 选择模型 → 开启智能路由 → 授权钥匙串 → 在 Codex 中验证**。

## 一、安装并授权 AiDoIt

### 步骤 1：安装应用并解除系统限制

打开安装包，将 `AiDoIt.app` 拖入 **Applications（应用程序）**。如果首次启动被 macOS 阻止，请进入 **系统设置 → 隐私与安全性**，点击 **仍要打开**。

![安装 AiDoIt 并在系统设置中允许打开](./images/1.png)

### 步骤 2：确认打开应用

系统再次弹出安全提示时，确认应用来源可信，然后点击 **仍要打开**。

![确认仍要打开 AiDoIt](./images/2.png)

## 二、添加 Provider

### 步骤 3：新建 Provider

进入 AiDoIt 的 **Codex 接入** 页面，点击右上角 **新增 Provider**。

![点击新增 Provider](./images/3.png)

### 步骤 4：填写连接信息

依次填写 Provider ID、显示名称、Base URL 和 API Key。macOS 上还需选择兼容协议：GPT 类模型通常选择 **Responses API**，Claude 类模型选择 **Messages**。填写后点击 **检测并获取模型**。

![填写 Provider 配置信息](./images/4.png)

### 步骤 5：选择要使用的模型

检测成功后，在模型列表中勾选需要注入 Codex 的模型；也可按需使用 **全选** 或 **清空**。

![勾选需要使用的模型](./images/5.png)

### 步骤 6：保存 Provider

确认模型选择无误后，点击右下角 **保存**。

![保存 Provider](./images/6.png)

## 三、启用智能路由

### 步骤 7：启动智能路由

看到“Provider 已保存”提示后，选择默认 Provider 和模型，再点击 **开启智能路由并启动 Codex**。

![开启智能路由并启动 Codex](./images/7.png)

### 步骤 8：确认退出并重新启动

AiDoIt 会退出当前 Codex/ChatGPT，并在完成配置迁移后重新启动。点击 **退出 Codex/ChatGPT 并开启** 继续。

![确认退出并开启智能路由](./images/8.png)

### 步骤 9：允许访问钥匙串

输入当前 macOS 登录密码，并点击 **始终允许**，让 AiDoIt 可以读取保存在钥匙串中的 Provider API Key。

![允许 AiDoIt 访问钥匙串](./images/9.png)

### 步骤 10：在 Codex 桌面端选择模型

重新启动后，打开模型菜单即可看到带 Provider 标识的第三方模型，选择需要使用的模型即可。

![在 Codex 桌面端选择第三方模型](./images/10.png)

### 步骤 11：在 Codex CLI 中选择模型

在 Codex CLI 的模型选择界面中，同样可以看到由 AiDoIt 注入的模型及对应兼容协议。

![在 Codex CLI 中选择第三方模型](./images/11.png)

## 四、无账号登录模式（可选）

### 步骤 12：打开无账号登录模式

如果没有 ChatGPT/Codex 登录账号，可返回 **Codex 接入** 页面，打开 **无账号登录模式** 开关。

![打开无账号登录模式](./images/121.png)

### 步骤 13：先关闭当前智能路由

若智能路由正在运行，按提示点击 **退出 Codex/ChatGPT 并关闭**，先恢复官方模型状态，再配置无账号模式。

![关闭当前智能路由](./images/13.png)

### 步骤 14：选择无账号模式使用的模型

开启无账号登录模式后，从已有 Provider 中选择需要显示的模型。可通过上下箭头调整顺序，第 1 个模型将作为默认模型。

![选择并排列无账号模式模型](./images/14.png)

### 步骤 15：应用配置并启动 Codex

确认模型及顺序后，点击 **开启智能路由并启动 Codex**。

![应用无账号模式配置并启动 Codex](./images/15.png)

### 步骤 16：确认路由已生效

Codex 启动后，左下角会显示 **AiDoIt Router**，输入框右侧会显示当前选中的 Provider 模型，表示路由已生效。

![确认 AiDoIt Router 已生效](./images/16.png)

## 五、恢复官方登录状态

### 步骤 17：关闭智能路由

如需切回官方登录和官方模型，返回 AiDoIt，点击 **关闭智能路由并恢复登录状态**。

![关闭智能路由并恢复登录状态](./images/17.png)

### 步骤 18：检查模型列表

重新进入 Codex 的模型选择界面，确认官方模型与配置的 Provider 模型显示正常，即完成全部配置。

![检查 Codex CLI 模型列表](./images/18.png)

## 常见问题

### macOS 阻止打开 AiDoIt

确认安装包来源可信后，进入 **系统设置 → 隐私与安全性**，在对应提示中选择 **仍要打开**。不要为来源不明的安装包绕过系统保护。

### 钥匙串授权反复出现

确认输入的是当前 macOS 登录密码，并在可信的 AiDoIt 进程请求中选择 **始终允许**。如果 Provider 凭据已变化，请在 AiDoIt 中重新保存。

### 路由开启后看不到 Provider 模型

完全退出 Codex 与 ChatGPT，回到 AiDoIt 关闭并重新开启智能路由，再启动 Codex 检查模型菜单。

## 下一步

- [接入 Claude（macOS）](../Claude/README.md)
- [Ubuntu 安装与使用](../../Ubuntu/README.md)
- [返回帮助中心](../../README.md)
