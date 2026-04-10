# Building the Nuvio TV Desktop App

This guide explains how to package the Nuvio TV codebase into a native desktop `.exe` or `.msi` application using Tauri.

## Prerequisites

To build the application from source, you must install the following on your system:

- **Node.js**: [Download here](https://nodejs.org/) (v18 or higher recommended)
- **Rust & Cargo**: [Download here](https://www.rust-lang.org/tools/install)
- **Microsoft C++ Build Tools**: Required on Windows during the Tauri setup process. Ensure you have the [Tauri Windows Prerequisites](https://tauri.app/v1/guides/getting-started/prerequisites) installed (C++ build tools and WebView2).

## Build Instructions

1. **Install Dependencies**  
   Open your terminal in the root directory of this project and run:
   ```bash
   npm install
   ```

2. **Package the Application**  
   Once all dependencies are installed, you can trigger the Tauri production compiler by running:
   ```bash
   npm run tauri:build
   ```
   *Note: This command will automatically compile the web assets before securely bundling the final native desktop wrapper. The compilation will take a few minutes.*

## Output Location

Once the build successfully completes, you will find your generated `.msi` system installer and standard `.exe` setup file in the following directories:

- **MSI Installer:** `src-tauri/target/release/bundle/msi/`
- **NSIS Setup:** `src-tauri/target/release/bundle/nsis/`
