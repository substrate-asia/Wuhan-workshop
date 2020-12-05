

# Prerequisite



## 报名须知

由于 Workshop 有线下编程环节，所以请携带电脑和提前安装好环境。

1、请携带电脑。虽然大会现场提供桌子和插线板，自带插线板最有保障。

2、请事先安装环境。环境配置要求如下：

Rust 安装：

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```



切换到指定 Rust 版本：

```bash
rustup install nightly-2020-10-06
rustup target add wasm32-unknown-unknown --toolchain nightly-2020-10-06
```



## 编译Substrate note template

```bash
# Clone the Substrate note template Repo
git clone https://github.com/substrate-developer-hub/substrate-node-template

## Switch into the directory an compile
cd substrate-node-template && cargo build --release

```



## 构造Relay chain

请执行一下命令来编译relay chain:

```bash
# Clone the Polkadot Repository
git clone https://github.com/paritytech/polkadot.git

# Switch into the Polkadot directory
cd polkadot

# Checkout the proper commit
git checkout 93f0029

# Setup proper Rust version for compiling this workshop


# Build the Relay Chain Node
cargo +nightly-2020-10-06 build --release

# Print the help page to ensure the node build correctly
./target/release/polkadot --help
```

如果成功打印帮助页面，则编译成功。



## 构造Parachain

```bash
# Clone the Parachain Template
git clone https://github.com/substrate-developer-hub/substrate-parachain-template.git

# Switch into the Parachain Template directory
cd substrate-parachain-template

# Checkout the proper commit
git checkout 9506b93

# Build the parachain template collator
cargo build --release

# Print the help page to ensure the node built correctly
./target/release/parachain-collator --help
```

如果成功打印帮助页面，则编译成功。

