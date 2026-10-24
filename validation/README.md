# Author inference comparison

The adapter uses the original v1.3.1 checkpoint and observation config with the current author's documented legacy RoPE window handling. `native-sources.json` pins the author files by SHA256. `validate_inference.py` compares 160 inputs, four resets, endpoint padding and recurrent-cache boundary transitions against the original author functions.

```bash
uv run validate_inference.py --source /path/to/pinned/HoloMotion --weights /path/to/motion_tracking_model.onnx --output /tmp/holo131-native.json
```

`legacy-window-check.json` records isolated boundary probes. Neither this probe nor the matched-input comparison replaces full motion rollout validation. The author max-length override is8192, with its default reset margin64; cache resets leave reference time and physical state unchanged.

Reports: `native-parity.json` (macOS), `native-parity-linux.json` (Linux).
