## Getting Started

Follow the steps below to get started.

### Rust toolchain 

https://docs.substrate.io/install/

### XCM Playground via Zombienet

Build the trappist repository with 
```
git clone -b xcm-demo --depth 1 https://github.com/paritytech/trappist
cd trappist && cargo build –-release
```

Leave in the `target/release` folder:
- `trappist-collator` (which you will build from the `trappist` repository) 

Create a `bin` directory into the root of the trappist repository and place the following binaries inside of it:
- `polkadot` (which you can download from [workshop files](https://github.com/lana-shanghai/workshop_files))
- `polkadot-collator` ([workshop_files](https://github.com/lana-shanghai/workshop_files))

Download the [latest release of zombienet](https://github.com/paritytech/zombienet/releases/) into the root of the trappist repository and make it executable:
```
$ chmod +x zombienet-linux # OR
$ chmod +x zombienet-macos
```

Then, start the playground with:
```
./zombienet-linux -p native spawn xcm-playground.toml
```

