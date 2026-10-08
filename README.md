# HDRI Studio models

Model files the HDRI Studio server downloads at image build time and checks against a pinned SHA-256.

## da3_metric_large_336x252.onnx

Depth Anything 3 Metric-Large exported to ONNX for the server's parallax engine (per-photo metric depth on the CPU
with ONNX Runtime).

- Release asset: `da3-metric-large-336x252-v1` → `da3_metric_large_336x252.onnx`
- SHA-256: `b99a4720f148ffaefaa9b7be534973ca26238be10b4c6a550c1d56cab69dcc8d`
- Size: 1,336,957,333 bytes
- Input `image`: float32 (1, 3, 336, 252), ImageNet-normalised RGB. Outputs `depth` and `sky`, each (1, 336, 252).
- Upstream weights: [depth-anything/DA3METRIC-LARGE](https://huggingface.co/depth-anything/DA3METRIC-LARGE)
  from [ByteDance-Seed/Depth-Anything-3](https://github.com/ByteDance-Seed/Depth-Anything-3), Apache License 2.0.

See [NOTICE](NOTICE) for attribution and changes. The weights are not modified; the file is a fixed-size ONNX export
with the network's final sky step switched off (the server performs it).
