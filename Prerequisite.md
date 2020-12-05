

# Prerequisite

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
rustup install nightly-2020-10-06
rustup target add wasm32-unknown-unknown --toolchain nightly-2020-10-06

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

