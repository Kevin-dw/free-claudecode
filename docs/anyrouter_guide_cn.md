# 在国内免费使用Claude Code指南

Claude Code 是 Anthropic 公司推出的一款强大的 AI 编程助手。由于网络限制，国内用户直接使用官方服务可能会遇到困难。本指南将向您展示如何在国内顺畅地免费使用 Claude Code。

---

### 第一步：注册 AnyRouter 并获取 API 密钥

1.  **访问 AnyRouter 平台**:
    首先，在浏览器中打开 AnyRouter 的注册页面：[https://anyrouter.top/register](https://anyrouter.top/register?aff=Oy79)。该平台为新用户提供免费试用额度，让您可以无成本体验。

2.  **生成您的专属密钥**:
    完成注册并登录后，进入控制台，找到 API 密钥管理部分。创建一个新的 API 密钥（通常以 `sk-` 开头），并复制保存好，稍后会用到。

---

### 第二步：安装 Node.js

要运行 Claude Code 命令行工具 (CLI)，您的电脑上需要有 Node.js 环境。

-   **Windows 用户**:
    访问 [Node.js 官网](https://nodejs.org/)，下载并安装适用于您系统的 LTS (长期支持) 版本。对于 Windows 用户，一路点击“下一步”即可完成安装。

-   **macOS / Linux 用户**:
    推荐使用您系统的包管理器来安装。
    ```bash
    # Ubuntu/Debian
    sudo apt update
    sudo apt install nodejs npm

    # macOS (使用 Homebrew)
    brew install node
    ```
    您可以通过在终端运行 `node -v` 和 `npm -v` 来验证安装是否成功。

---

### 第三步：安装 Claude Code CLI

接下来，打开您的终端（在 Windows 上是 `CMD` 或 `PowerShell`），然后执行以下命令，全局安装 Claude Code 命令行工具：

```bash
npm install -g @anthropic-ai/claude-code
```

---

### 第四步：配置关键环境变量

这是配置过程中的核心环节。我们需要设置两个关键的环境变量，以将 Claude Code CLI 的请求指向 AnyRouter 的服务地址。

-   `ANTHROPIC_AUTH_TOKEN`: 您在第一步中从 AnyRouter 获取的 API 密钥。
-   `ANTHROPIC_BASE_URL`: AnyRouter 平台的 API 地址，即 `https://anyrouter.top`。

#### **Windows（WSL） 用户配置**

**方法一：临时配置 (当前终端有效)**

在 `CMD` 终端中执行：

```cmd
set ANTHROPIC_AUTH_TOKEN=你的API密钥
set ANTHROPIC_BASE_URL=https://anyrouter.top
```
请将 `你的API密钥` 替换为您自己的密钥。

**方法二：永久配置 (推荐)**

为了长久生效，避免每次打开终端都需重复设置，推荐使用 `setx` 命令进行永久性配置。请注意：通过 `setx` 设置的变量只在 **新创建** 的终端会话中生效。

```cmd
setx ANTHROPIC_AUTH_TOKEN "你的API密钥"
setx ANTHROPIC_BASE_URL "https://anyrouter.top"
```

#### **macOS / Linux 用户配置**

**方法一：临时配置**

```bash
export ANTHROPIC_AUTH_TOKEN='你的API密钥'
export ANTHROPIC_BASE_URL='https://anyrouter.top'
```

**方法二：永久配置**

将上述 `export` 命令添加到您 shell 的配置文件中（如 `~/.bashrc`, `~/.zshrc`）。

```bash
echo "export ANTHROPIC_AUTH_TOKEN='你的API密钥'" >> ~/.zshrc
echo "export ANTHROPIC_BASE_URL='https://anyrouter.top'" >> ~/.zshrc
source ~/.zshrc # 使配置立即生效
```

---

### 第五步：启动并开始编码

一切准备就绪！现在可以启动 Claude Code 了。

1.  **打开新终端**: 重新打开一个终端窗口，确保环境变量已加载。
2.  **进入项目目录**: 使用 `cd` 命令导航到您的代码项目文件夹。
3.  **运行 Claude**: 输入以下命令即可启动：
    ```bash
    claude
    ```

如果配置正确，您将看到 Claude Code 的欢迎界面，现在可以开始与它对话，让它帮助您编码了。祝您编码愉快！ 