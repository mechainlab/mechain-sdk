# Mechain SDK

The SDK includes zk-dsl bindings to the Wallet API.



`Mechain SDK` uses the `ff` and `group` crates to build circuits generically over a
scalar field type, which is used as the "word" of a circuit. Arithmetic
operations modulo the scalar field's prime are efficient, while other operations
(such as boolean logic) are implemented using these words.


#### Javascript Wallet Bindings

The core logic of the sdk is written in Rust and built from mechain-wallet, based on bellman lib. To integrate it into Javascript we use the wasm-bindgen crate to build the WASM Foreign-Function Interface and then call the WASM functions from Javascript.

Note: Data Library has been deprecated.