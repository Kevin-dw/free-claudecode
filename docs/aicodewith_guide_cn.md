# 国内免费使用 Claude Code一键安装方案

Claude Code 是 Anthropic 公司推出的一款强大的 AI 编程助手。由于网络限制，国内用户直接使用官方服务可能会遇到困难。本指南将向您展示如何在国内顺畅地免费使用 Claude Code。

[**aicodewith 官方镜像站**](https://aicodewith.com/?invitation=MKFA9DI)

---

### 第一步：注册并准备

在使用一键安装脚本之前，请先访问 [aicodewith.com](https://aicodewith.com/?invitation=MKFA9DI) 并完成注册。平台为新用户提供了免费的体验额度。注册后，您可能需要获取一个凭证或API密钥，请按照平台的指引操作，并在安装过程中根据脚本提示使用。

---

### 第二步：执行一键安装脚本

`aicodewith.com` 提供了针对主流操作系统的自动化安装脚本。请根据您的系统选择对应的命令。

#### 1. Linux 用户

此脚本适用于大多数主流 Linux 发行版（如 Ubuntu, CentOS, Debian 等）。

-   **安装命令**
    ```bash
    curl -fsSL https://aicodewith.com/claudecode/resources/install-script-linux | bash
    ```
-   **操作指南**
    1.  打开您的 Linux 终端。
    2.  复制并粘贴以上命令，然后按回车执行。
    3.  脚本将自动处理所有依赖和配置，请耐心等待其完成。

#### 2. macOS 用户

对于 macOS 用户，脚本同样可以为您自动化整个安装过程。

-   **安装命令**
    ```bash
    curl -fsSL https://aicodewith.com/claudecode/resources/install-script-macos | bash
    ```
-   **操作指南**
    1.  打开“终端”应用程序。
    2.  将上面的命令粘贴进去并执行。
    3.  如果网络访问不佳，建议在执行前开启网络代理。

#### 3. Windows (WSL) 用户

Windows 用户需要通过 WSL (Windows Subsystem for Linux) 环境来运行脚本。

-   **系统要求**
    - 确保您的 Windows 系统已成功安装并配置了 WSL2 及一个 Linux 发行版（例如 Ubuntu）。
-   **安装命令**
    ```bash
    curl -fsSL https://aicodewith.com/claudecode/resources/install-script-wsl | bash
    ```
-   **操作指南**
    1.  从开始菜单启动您的 WSL 终端（如 Ubuntu）。
    2.  在打开的终端窗口中，粘贴并运行上述命令。
    3.  脚本会自动在 WSL 环境中完成所有设置。

---

### 第三步：开始使用 Claude Code

安装脚本执行完毕后，通常 Claude Code 就已经准备就绪了。

1.  **重启终端**: 为了确保所有环境配置都已生效，建议您关闭当前终端并重新打开一个新的。
2.  **启动 Claude**: 在终端里直接运行以下命令：
    ```bash
    claude
    ```
3.  **开始对话**: 如果一切顺利，Claude Code 将会启动，您就可以开始与 AI 进行编程对话了。 