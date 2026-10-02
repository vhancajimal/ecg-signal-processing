# ECG Signal Processing

Biomedical signal processing project focused on ECG analysis using Python and public data from the MIT-BIH Arrhythmia Database.

## Project Goals

This project explores basic ECG signal processing techniques, including:

- ECG visualization
- R-peak detection
- RR interval calculation
- Heart-rate estimation
- Basic physiological signal analysis

## Dataset

The project uses ECG recordings from the MIT-BIH Arrhythmia Database available through PhysioNet.

## Tools

- Python
- NumPy
- Matplotlib
- WFDB
- Jupyter Notebook
- Git / GitHub

## Current Results

A first analysis was performed using MIT-BIH record 100.

The workflow:

1. Load the ECG signal
2. Visualize the raw ECG
3. Detect R-peaks using a simple threshold-based method
4. Calculate RR intervals
5. Estimate beat-to-beat heart rate

The estimated average heart rate in the analyzed segment was approximately:

**74.6 BPM**

## Repository Structure

```text
ecg-signal-processing/
├── data/
├── notebooks/
│   └── 01_ecg_visualization.ipynb
├── results/
├── src/
└── README.md
```text

## Limitations

The current R-peak detector is a simple first implementation based on amplitude thresholding and minimum peak distance.

## Future Improvements

- ECG filtering
- more robust R-peak detection
- comparison with reference annotations
- heart-rate variability analysis
- longer ECG recordings
- feature extraction
- arrhythmia classification

## Status

Work in progress.
