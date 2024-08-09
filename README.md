# 0g-da-retriever-guide

![0G-Labs](https://github.com/user-attachments/assets/4ab23161-cd06-4829-90c5-535d235138e4)


### 🛠️ DA Retriever Setup Guide

This document provides a step-by-step guide for setting up and running your own DA retriever. Let’s get started! 🚀

### 🖥️ Recommended Hardware Specifications

For optimal performance, it is recommended that your system meets the following specifications:

- **💾 RAM:** 8 GB
- **🧠 CPU:** 2 cores
- **📡 Bandwidth:** 100 Mbps for both download and upload

### 🛠️ Installation

#### 📥 Install Dependencies

##### 🐧 For Linux

1. Update your package manager:
   ```bash
   sudo apt-get update
   ```
2. Install necessary packages:
   ```bash
   sudo apt-get install cmake build-essential protobuf-compiler
   ```

##### 🍏 For macOS

1. Install cmake using Homebrew:
   ```bash
   brew install cmake
   ```

#### 🦀 Install Rust

1. Use the following command to install Rust:
   ```bash
   curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
   ```

### 📦 Download the Source Code

Clone the repository containing the source code:
```bash
git clone https://github.com/0glabs/0g-da-retriever.git
```

### ⚙️ Configuration

Here are the key configuration parameters you need to be aware of:

| Field                 | Description                                                  |
|-----------------------|--------------------------------------------------------------|
| `log_level`           | Set the log level (e.g., `info`, `debug`, `warn`, `error`).   |
| `grpc_listen_address` | Address where the server will listen for incoming connections.|
| `eth_rpc_endpoint`    | JSON RPC node endpoint for the blockchain network.            |

### 🚀 Running the DA Retriever

#### 🛠️ Build in Release Mode

To build the retriever in release mode, run the following command:
```bash
cargo build --release
```

#### ▶️ Run the Retriever

1. Update the configuration file located at `run/config.toml` with your desired settings, using the parameters mentioned in the Configuration section. 
2. Start the retriever with the following command:
   ```bash
   ./target/release/retriever --config ./run/config.toml
   ```

🎉 Congratulations! Your DA retriever is now up and running.
