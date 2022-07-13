# Denoflate

WebAssembly powered Deflate/Gzip/Zlib compression for Deno, written in Rust.

## Usage

    deno cache -r https://deno.land/x/denoflate/mod.ts

```typescript
import { deflate, inflate } from "https://deno.land/x/denoflate/mod.ts";
// or { gzip, gunzip }
// or { zlib, unzlib }

const bytes = new Uint8Array([1, 2, 3]);
const compressed = deflate(bytes, undefined);
const decompressed = inflate(compressed);
```

## Test

> deno task test

## Building
  
First, install wasm-pack

```bash
curl https://rustwasm.github.io/wasm-pack/installer/init.sh -sSf | sh
```

> (From https://rustwasm.github.io/wasm-pack/installer/)

Then, run the task:

`deno task build`