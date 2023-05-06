---
description: Introduction to Proton
---

# Introduction

## What is Proton?

Proton is a layer one proof-of-stake blockchain that leverages cutting-edge [WebAssembly (WASM)](https://webassembly.org) smart contracts to enable high-performant, scalable and sustainable computation. Developers can leverage Proton to easily and securely build tokens, NFTs, exchanges, lending markets and much more.

Proton Smart Contracts use [AssemblyScript](https://www.assemblyscript.org/), a state of the art extension to [Typescript](https://www.typescriptlang.org/) that:
1. builds to high performance WASM
2. adds native types like u8, u16, u32, u64
3. integrates with the existing web ecosystem

## Basic Smart Contract
A simple Proton smart contract has the structure:

```ts
import { Contract, print } from 'proton-tsc'

@contract("hello")
class HelloContract extends Contract {
    @action("say")
    say(text: string): void {
        print(text);
    }
}
```

To generate the WASM and ABI that you can upload to the Proton blockchain, simply run:
```sh
npx proton-asc hello.ts
```

Ready to begin your journey? Head on over to [get started](./getting-started.md)!
