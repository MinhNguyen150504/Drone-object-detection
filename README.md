# Drone Object Detection

Object detection on drone (aerial) imagery using YOLO. This project explores how modern deep-learning detectors handle the challenges of aerial views: small objects, varied altitudes, dense scenes and occlusion. It is a personal learning project with an AI/ML focus and an aerospace-oriented application.

> **Status:** 🚧 In progress. Baseline model under development.

## Goals

- Build an end-to-end object detection pipeline: data preparation, training, evaluation, inference.
- Train and evaluate a baseline YOLO model on a drone-imagery dataset.
- Analyze failure cases (especially small and occluded objects) and improve the model.
- Keep the repository reproducible and well documented.

## Demo

_Sample detection results will be added here after the baseline is trained._

<!-- ![demo](results/demo.jpg) -->

## Dataset

- Dataset: [VisDrone](https://github.com/VisDrone/VisDrone-Dataset) (a subset is used for quick experiments).
- Raw data is **not** stored in this repo. See `data/README.md` (to be added) for download and preparation steps.

## Project Structure

```
drone-object-detection/
├── data/          # dataset config and preparation notes (raw data is git-ignored)
├── notebooks/     # exploratory data analysis and experiments
├── src/           # scripts: data conversion, training, inference
├── results/       # metrics, plots, sample predictions
├── docs/          # notes and documentation
├── requirements.txt
└── README.md
```

## Getting Started

```bash
git clone https://github.com/MinhNguyen150504/drone-object-detection.git
cd drone-object-detection
python -m venv .venv
source .venv/bin/activate      # Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

Training and inference commands will be added once the baseline is ready.

## Results

| Model   | Dataset subset | mAP@0.5 | mAP@0.5:0.95 | Notes    |
|---------|----------------|---------|--------------|----------|
| YOLOv8n | TBD            | TBD     | TBD          | Baseline |

## Roadmap

- [x] Initialize repository
- [ ] Explore dataset (class distribution, object sizes)
- [ ] Convert annotations to YOLO format
- [ ] Train baseline model (YOLOv8n)
- [ ] Evaluate and analyze failure cases
- [ ] Improve small-object detection (higher resolution, tiling, larger model)
- [ ] Export model (ONNX) and test on video

## Tech Stack

Python, PyTorch, Ultralytics YOLO, OpenCV, NumPy, Pandas, Matplotlib

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
