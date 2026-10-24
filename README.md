# HoloMotion v1.3.1

[Author project](https://github.com/HorizonRobotics/HoloMotion) · [Checkpoint](https://huggingface.co/HorizonRobotics/HoloMotion_models/blob/e3c90dd1f7483d02d3b4d2e5fb3a359c6ff9c67a/HoloMotion_motion_tracking_model_v1.3.1/exported/motion_tracking_model.onnx) · [Provenance](provenance.json)

## Install and run

```bash
git clone --recurse-submodules https://github.com/MotionChallenge-Project/MotionChallenge-holomotion-v1-3-1.git
cd MotionChallenge-holomotion-v1-3-1
uv sync
uv run evaluate.py
```

Produces success, completion and six MPBPE values in a verified `result.json`.
MuJoCo 3.17 CPU batch; `--jobs 8` sets parallelism. Missing data and weights are
downloaded and hash-checked; results and traces stay outside Git.

[Inference validation](validation/README.md) · [Native parity report](validation/native-parity.json)

## Observations

Ideal proprioception, without robot world-position or contact feedback. [Checkpoint requirements](admission.json) · [Rules](MotionChallenge-Core/docs/OBSERVATIONS.md).
