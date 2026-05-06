# Bonus — Thread sweep

Model: `qwen2.5-1.5b-instruct-q4_k_m.gguf`  ·  GPU layers: `0`

| threads | tg64 (tok/s) |
|---:|---:|
| 1 | 7.3 |
| 2 | 22.4 |
| 6 | 37.6 |
| 12 | 41.6 |
| 16 | 39.9 |
| 32 | 33.7 |

**Best**: `-t 12` at 41.6 tok/s.

Look at the curve. If it peaks around your **physical** core count and drops as you go higher, that's the memory-bandwidth ceiling: extra threads fight over the same memory channels and slow each other down.
