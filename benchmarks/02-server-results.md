# 02 - Server Results

Run: `python 02-llama-cpp-server/record-metrics.py --duration 60`

Result: scrape failed (no samples collected). The server was not reachable with `/metrics` or was not started with `--metrics`, so no CSV was produced and no KV-cache peak can be reported.

## KV-cache observation

- Peak `llamacpp:kv_cache_usage_ratio`: N/A (no metrics samples).
