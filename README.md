# Rust LLVM hello, world

LLVM code see in [main.ll](main.ll)

## Setup

## Install LLVM

```
brew install cmake ninja
```

### remote

```bash
cargo install llvmenv
```

usage

```
llvmenv init
llvmenv entries
local-llvm 10.0.0
```

about `1.5 hours` in my MBP 2018

### local

Add local llvm for build to: `$XDG_CONFIG_HOME/llvmenv/entry.toml

docs: https://docs.rs/llvmenv/0.3.0/llvmenv/entry/index.html

````
[local-llvm]
path = "/path/to/your/src"
target = ["X86"]
```

**build**

```
llvmenv build-entry local-llvm
```

### run & build

```
LLVM_SYS_100_PREFIX=$HOME/llvm/llvm-10.0.1.src/build cargo build
LLVM_SYS_100_PREFIX=$HOME/llvm/llvm-10.0.1.src/build cargo run
````
