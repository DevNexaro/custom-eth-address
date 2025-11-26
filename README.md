![Banner](./image.png)

# Custom ETH Address Generator ⚡

A **fully client-side Ethereum vanity address generator**, accelerated with low-level **WebAssembly + SIMD** and highly optimized C++ → WASM kernels.  
Built to deliver “GPU-like” speed directly in your browser — no servers, no backend, no key transmission.

Generate clean, custom Ethereum addresses such as:

```
0x0000...
0xDEAD...
0xCAFE...
0xSOL...
0xBABE...
```

Perfect for **branding**, **security**, or simply having a unique and recognizable wallet.

---

## Try it instantly 

👉 **https://customethaddress.com**

All computation happens client-side using:

- WebAssembly (WASM)
- SIMD acceleration (AVX2 / AVX512 where available)
- Multi-threaded Web Workers
- Hand-tuned inner loops inspired by high‑performance GPU kernels

No private key ever leaves your device.

---

## Features

- **WASM-accelerated prefix/suffix search**
- Keys generated fully client-side
- Supports combined patterns (prefix + suffix)
- Instant Web UI — no installation required
- Ethereum-compatible (secp256k1)

---

## Why this exists

Most vanity generators are either:

- **GPU miners** → fast but require setup + trust  
- **Browser-only** → too slow for real vanity mining  
- **Unoptimized** → waste cycles, poor SIMD usage  

This project fixes all that using:

- WASM-optimized C++ kernels  
- Manual SIMD intrinsics  
- Multi-threaded workers  
- No backend dependency  
- Zero-trust architecture  

Inspired by **profanity2**, but re-engineered for **modern browsers with a native-like execution pipeline**.

---

## How it works

1. You enter a pattern (e.g., `0x0000`, `0xBABE`, `0xALPHA`)
2. The WASM engine brute-forces millions of keys per second
3. Once a match hits:
   - The public address is displayed  
   - The private key (generated locally) is shown  
4. You save it securely

Everything happens **in-memory only** — no server, no logs.

---

## Performance Benchmarks

| Hardware (Browser) | 4-char Prefix | 5-char Prefix | 6-char Prefix |
|-------------------|----------------|----------------|----------------|
| Basic laptop CPU   | slow           | very slow      | impractical    |
| High-end laptop    | decent         | slow           | very slow      |
| Desktop CPU (AVX2) | fast           | manageable     | slow           |
| AVX-512 CPU        | **very fast**  | **fast**       | realistic      |

With the optimized WASM pipeline, performance is several times higher than typical JS-based miners.

---

## SEO Coverage

This README naturally ranks for:

- client-side ETH address generator
- ethereum vanity address tool
- wasm ethereum vanity generator
- webassembly eth wallet generator
- eth vanity browser tool
- fast ethereum key generator
- profanity2 inspired eth vanity

---

## Credits

Inspired by 1inch & profanity2.  
Live client-side implementation: https://customethaddress.com
