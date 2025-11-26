# 🛠️ Development Environment Setup Guide

This guide provides instructions for setting up the required development environment components on **Windows** and **Linux** systems.

## Required Component Versions

| Component | Version | Notes |
| :--- | :--- | :--- |
| **NVM** (Node Version Manager) | `0.40.3` | Used to manage multiple Node.js versions. |
| **Node.js** | `22.19.0` | Installed via NVM. |
| **npm** | `11.6.0` | The version compatible with Node.js `22.19.0` is typically installed automatically. We will install the specific npm version after Node.js. |
| **Angular CLI** | `20.3.2` | Installed globally via npm. |
| **TypeScript** | `5.2.8` | Installed globally via npm. |

---

## 1. Windows Installation (using nvm-windows)

On Windows, we use a separate project called **nvm-windows** (or `nvm-setup.exe`) which is distinct from the Linux/macOS `nvm` project.

### 1.1. Install nvm-windows

1.  **Uninstall Existing Node.js:** If you have an existing Node.js installation, uninstall it from **"Add or remove programs"** to prevent conflicts.
2.  **Download the Installer:**
    * Go to the [nvm-windows releases page](https://github.com/coreybutler/nvm-windows/releases).
    * Download the `nvm-setup.exe` file from the **Assets** section of the latest release (or the one that includes a compatible NVM version).
3.  **Run Installer:** Run the downloaded `nvm-setup.exe` and follow the prompts. You can typically accept the default installation paths.
4.  **Verify Installation:** Open a **new** command prompt or PowerShell window and run:
    ```bash
    nvm version
    ```
    This should show the nvm-windows version.

### 1.2. Install Node.js and npm

1.  **Install Node.js `22.19.0`:**
    ```bash
    nvm install 22.19.0
    ```
2.  **Use Node.js `22.19.0`:**
    ```bash
    nvm use 22.19.0
    ```
3.  **Verify Node.js Version:**
    ```bash
    node -v
    ```
    The output should be `v22.19.0`.
4.  **Install/Update npm to `11.6.0`:**
    Node.js `22.19.0` may install a different npm version. Update it globally:
    ```bash
    npm install -g npm@11.6.0
    ```
5.  **Verify npm Version:**
    ```bash
    npm -v
    ```
    The output should be `11.6.0`.

### 1.3. Install Angular CLI and TypeScript

Install Angular CLI and the specified TypeScript version globally.

1.  **Install Angular CLI `20.3.2`:**
    ```bash
    npm install -g @angular/cli@20.3.2
    ```
2.  **Install TypeScript `5.2.8`:**
    ```bash
    npm install -g typescript@5.8
    ```
3.  **Verify Global Packages:**
    ```bash
    ng version
    tsc -v
    ```
    * `ng version` should show **Angular CLI: 20.3.2**
    * `tsc -v` should show **Version 5.8**

---

## 2. Linux Installation (using nvm-sh/nvm)

This section uses the official POSIX-compliant **nvm** (Node Version Manager) for Linux.

### 2.1. Install NVM `0.40.3`

1.  **Install/Update Script:** Open your terminal and run the following `curl` command to download and run the install script for NVM version `v0.40.3`.
    ```bash
    curl -o- [https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh](https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh) | bash
    ```
    *Alternatively, you can use `wget`:*
    ```bash
    wget -qO- [https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh](https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh) | bash
    ```
2.  **Source NVM:** After the script finishes, **close and reopen your terminal** or run the following command to source the NVM script:
    ```bash
    export NVM_DIR="$HOME/.nvm"
    [ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
    [ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion" # This loads nvm bash_completion
    ```
    *Note: The install script attempts to add these lines to your profile file (`~/.bashrc`, `~/.zshrc`, etc.) automatically.*
3.  **Verify Installation:**
    ```bash
    nvm --version
    ```
    The output should be `0.40.3`.

### 2.2. Install Node.js and npm

1.  **Install Node.js `22.19.0`:**
    ```bash
    nvm install 22.19.0
    ```
    This command installs Node.js and the npm version bundled with it.
2.  **Use Node.js `22.19.0`:**
    ```bash
    nvm use 22.19.0
    ```
3.  **Verify Node.js Version:**
    ```bash
    node -v
    ```
    The output should be `v22.19.0`.
4.  **Install/Update npm to `11.6.0`:**
    Node.js `22.19.0` may install a different npm version. Update it globally:
    ```bash
    npm install -g npm@11.6.0
    ```
5.  **Verify npm Version:**
    ```bash
    npm -v
    ```
    The output should be `11.6.0`.

### 2.3. Install Angular CLI and TypeScript

Install Angular CLI and the specified TypeScript version globally.

1.  **Install Angular CLI `20.3.2`:**
    ```bash
    npm install -g @angular/cli@20.3.2
    ```
2.  **Install TypeScript `5.2.8`:**
    ```bash
    npm install -g typescript@5.2.8
    ```
3.  **Verify Global Packages:**
    ```bash
    ng version
    tsc -v
    ```
    * `ng version` should show **Angular CLI: 20.3.2**
    * `tsc -v` should show **Version 5.2.8**
