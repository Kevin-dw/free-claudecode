 # Guide to Using Claude Code for Free (Windows & macOS/Linux)


### Step 1: Register and Get an API Key

1.  **Visit the Registration Page**:
    Open your browser and go to [https://anyrouter.top](https://anyrouter.top/register?aff=Oy79) to register. According to the platform's current policy, new users can receive a certain amount of free credit.

2.  **Create an API Key**:
    After registering and logging in, find the API key management function on the platform's dashboard or a related page and create a new API key. This key usually starts with `sk-`, please keep it safe.

---

### Step 2: Install the Node.js Environment

To use the Claude Code command-line tool (CLI), you need to install Node.js first.

-   **For Windows Users**:
    Visit the [Node.js official website](https://nodejs.org/), download the recommended LTS (Long-Term Support) version, and install it. The installation process is mostly just clicking "next".

-   **For macOS / Linux Users**:
    You can use a package manager for installation, for example:
    ```bash
    # Ubuntu/Debian
    sudo apt update
    sudo apt install nodejs npm

    # macOS (using Homebrew)
    brew install node
    ```
    After installation, you can check if it was successful with the `node -v` and `npm -v` commands.

---

### Step 3: Install the Claude Code CLI

Open your terminal (Windows users can use `CMD` or `PowerShell`) and run the following command to globally install the Claude Code command-line tool:

```bash
npm install -g @anthropic-ai/claude-code
```

---

### Step 4: Configure Environment Variables and Run

This is the most crucial step. You need to configure two environment variables so that the CLI tool can correctly connect to the `AnyRouter` platform.

-   `ANTHROPIC_AUTH_TOKEN`: The API key you obtained in the first step.
-   `ANTHROPIC_BASE_URL`: The API address of the AnyRouter platform, which is `https://anyrouter.top`.

#### **Configuration for Windows Users**

**Method 1: Temporary Configuration (only valid in the current terminal window)**

Open a `CMD` terminal and execute the following commands:

```cmd
set ANTHROPIC_AUTH_TOKEN=your_api_key
set ANTHROPIC_BASE_URL=https://anyrouter.top
```
Replace `your_api_key` with your own key.

**Method 2: Permanent Configuration (Recommended)**

To avoid having to set the variables every time, you can use the `setx` command to save them permanently in the system. **Note: Variables set with `setx` will only take effect in new terminal windows.**

```cmd
setx ANTHROPIC_AUTH_TOKEN "your_api_key"
setx ANTHROPIC_BASE_URL "https://anyrouter.top"
```
Again, please replace `your_api_key`.

#### **Configuration for macOS / Linux Users**

**Method 1: Temporary Configuration**

```bash
export ANTHROPIC_AUTH_TOKEN='your_api_key'
export ANTHROPIC_BASE_URL='https://anyrouter.top'
```

**Method 2: Permanent Configuration**

Add the `export` commands above to your shell configuration file, such as `~/.bashrc`, `~/.zshrc`, or `~/.profile`.

```bash
echo "export ANTHROPIC_AUTH_TOKEN='your_api_key'" >> ~/.zshrc
echo "export ANTHROPIC_BASE_URL='https://anyrouter.top'" >> ~/.zshrc
source ~/.zshrc # Make the configuration effective immediately
```

---

### Step 5: Start Using

1.  Open a new terminal window (especially if you used `setx` or modified your shell configuration file).
2.  Use the `cd` command to navigate to the directory where your project code is located.
3.  Run the following command to start Claude Code:
    ```bash
    claude
    ```

If everything goes well, Claude Code will start and be ready to interact with you.
