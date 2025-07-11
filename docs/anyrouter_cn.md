
# 免费使用 Claude Code 指南 (Windows & macOS/Linux)


### 第一步：注册并获取 API 密钥

1.  **访问注册页面**:
    打开浏览器，访问 [https://anyrouter.top](https://anyrouter.top/register?aff=Oy79) 进行注册。根据平台目前的政策，新用户可以获得一定的免费额度。

2.  **创建 API 密钥**:
    注册并登录后，在平台的仪表盘或相关页面找到 API 密钥管理功能，创建一个新的 API 密钥。这个密钥通常以 `sk-` 开头，请妥善保管。

---

### 第二步：安装 Node.js 环境

要使用 Claude Code 的命令行工具 (CLI)，您需要先安装 Node.js。

-   **对于 Windows 用户**:
    访问 [Node.js 官网](https://nodejs.org/)，下载推荐的 LTS (长期支持) 版本并安装。安装过程基本是下一步即可。

-   **对于 macOS / Linux 用户**:
    可以使用包管理器进行安装，例如：
    ```bash
    # Ubuntu/Debian
    sudo apt update
    sudo apt install nodejs npm

    # macOS (使用 Homebrew)
    brew install node
    ```
    安装完成后，可以通过 `node -v` 和 `npm -v` 命令检查是否安装成功。

---

### 第三步：安装 Claude Code CLI

打开您的终端 (Windows 用户可以使用 `CMD` 或 `PowerShell`)，运行以下命令来全局安装 Claude Code 的命令行工具：

```bash
npm install -g @anthropic-ai/claude-code
```

---

### 第四步：配置环境变量并运行

这是最关键的一步。您需要配置两个环境变量，以便 CLI 工具能够正确地连接到 `AnyRouter` 平台。

-   `ANTHROPIC_AUTH_TOKEN`: 您在第一步中获取的 API 密钥。
-   `ANTHROPIC_BASE_URL`: AnyRouter 平台的 API 地址，即 `https://anyrouter.top`。

#### **Windows 用户配置方法**

**方法一：临时配置 (仅在当前终端窗口有效)**

打开 `CMD` 终端，执行以下命令：

```cmd
set ANTHROPIC_AUTH_TOKEN=你的API密钥
set ANTHROPIC_BASE_URL=https://anyrouter.top
```
将 `你的API密钥` 替换为您自己的密钥。

**方法二：永久配置 (推荐)**

为了避免每次都重新设置，可以使用 `setx` 命令将变量永久保存在系统中。**注意：`setx` 设置的变量在新的终端窗口中才会生效。**

```cmd
setx ANTHROPIC_AUTH_TOKEN "你的API密钥"
setx ANTHROPIC_BASE_URL "https://anyrouter.top"
```
同样，请替换 `你的API密钥`。

#### **macOS / Linux 用户配置方法**

**方法一：临时配置**

```bash
export ANTHROPIC_AUTH_TOKEN='你的API密钥'
export ANTHROPIC_BASE_URL='https://anyrouter.top'
```

**方法二：永久配置**

将上述 `export` 命令添加到您的 shell 配置文件中，例如 `~/.bashrc`, `~/.zshrc` 或 `~/.profile`。

```bash
echo "export ANTHROPIC_AUTH_TOKEN='你的API密钥'" >> ~/.zshrc
echo "export ANTHROPIC_BASE_URL='https://anyrouter.top'" >> ~/.zshrc
source ~/.zshrc # 使配置立即生效
```

---

### 第五步：开始使用

1.  打开一个新的终端窗口 (特别是如果您使用了 `setx` 或修改了 shell 配置文件)。
2.  使用 `cd` 命令进入您的项目代码所在的目录。
3.  运行以下命令启动 Claude Code：
    ```bash
    claude
    ```

如果一切顺利，Claude Code 将会启动，并准备好与您进行交互。

