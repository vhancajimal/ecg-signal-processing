# ECG Signal Processing

A small biomedical signal-processing project using ECG data from the
MIT-BIH Arrhythmia Database.

The project demonstrates a basic pipeline for ECG preprocessing,
R-peak detection, heart-rate estimation, and validation against
reference beat annotations.

## Project Goals

- Load and visualize real ECG data
- Reduce baseline drift and high-frequency noise
- Detect R-peaks automatically
- Calculate RR intervals and heart rate
- Compare detected beats with MIT-BIH reference annotations

## Dataset

The project uses **Record 100** from the MIT-BIH Arrhythmia Database,
accessed through the WFDB Python package.

The current analysis uses a **15-second ECG segment**.

## Signal Processing Pipeline

1. Load ECG data
2. Apply a 0.5–40 Hz Butterworth band-pass filter
3. Detect R-peaks using `scipy.signal.find_peaks`
4. Calculate RR intervals
5. Estimate beat-to-beat heart rate
6. Compare detections with reference annotations
7. Evaluate detector performance

## Current Results

For the analyzed 15-second segment of Record 100:

- Reference beats: 19
- True positives: 19
- False positives: 0
- False negatives: 0
- Sensitivity: 100%
- Positive Predictive Value (PPV): 100%

These results apply only to this segment and should not be interpreted
as overall detector performance across the MIT-BIH database.

## Tools

- Python
- NumPy
- SciPy
- Matplotlib
- WFDB
- Jupyter Notebook
- Git / GitHub

## Repository Structure

```text
ecg-signal-processing/
├── notebooks/
│   └── 01_ecg_signal_processing.ipynb
├── data/
├── results/
├── src/
├── README.md
└── requirements.txt
```

## Limitations

The current implementation is a proof of concept based on a single, short ECG segment.

The detection parameters have not yet been validated across different patients, rhythms, ECG morphologies, or noise conditions.

## Future Work

Planned improvements include:

- Evaluate additional MIT-BIH records
- Analyze longer ECG recordings
- Test parameter robustness
- Perform heart-rate variability analysis
- Extract additional ECG features
- Explore arrhythmia classification

## Status

Work in progress.

The project will be expanded progressively as additional signal-processing methods are implemented.
