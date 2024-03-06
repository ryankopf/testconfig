# Bug Demonstration

1. Create a workspace project, with two sub projects.
2. One of the subprojects targets wasm, the other targets any PC (in my case, Windows)
3. Rust Analyzer refuses to process, because it does not load the .cargo/config.toml file in test_warp.

## Run / Test

This works:
wasm-pack build test_wasm --target web

This works:
cargo run test_warp

However, Rust Analyzer gives an error, and stops processing:
`wasm-bindgen` cannot be used for non-WASM target