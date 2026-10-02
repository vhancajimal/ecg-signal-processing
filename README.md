# ECG Signal Processing

Biomedical signal processing project focused on ECG analysis using Python and public data from the MIT-BIH Arrhythmia Database.

## Project Goals

This project explores basic ECG signal processing techniques, including:

- ECG visualization
- R-peak detection
- RR interval calculation
- heart-rate estimation
- basic physiological signal analysis

## Dataset

The project uses ECG recordings from the **MIT-BIH Arrhythmia Database**, accessed through the WFDB library.

## Tools

- Python
- NumPy
- Matplotlib
- WFDB
- Jupyter Notebook
- Git
- GitHub

## Current Results

A first analysis was performed using **MIT-BIH Record 100**.

The current workflow:

1. Load a public ECG recording
2. Visualize the ECG signal
3. Detect R-peaks using a simple threshold-based method
4. Calculate RR intervals
5. Estimate beat-to-beat heart rate
6. Visualize the estimated heart rate over time

The estimated average heart rate in the analyzed segment was approximately:

**74.6 BPM**

### Detection Performance

The R-peak detector was compared with the reference beat annotations from MIT-BIH Record 100.

For the analyzed segment:

- True positives: 37
- False positives: 0
- False negatives: 0
- Sensitivity: 100%
- Positive Predictive Value (PPV): 100%

These results are specific to the analyzed segment and do not represent performance across the full database.

## Repository Structure

```text
ecg-signal-processing/
├── data/
├── notebooks/
│   └── 01_ecg_visualization.ipynb
├── results/
├── src/
└── README.md
```

## Limitations

The current R-peak detector is a simple first implementation based on amplitude thresholding and minimum peak distance.

It is intended as an introductory implementation and is not designed for clinical use or robust ECG analysis.

## Future Improvements

Planned improvements include:

- ECG filtering
- more robust R-peak detection
- comparison with reference annotations
- heart-rate variability analysis
- analysis of longer ECG recordings
- ECG feature extraction
- arrhythmia classification

## Status

Work in progress.

The project will be expanded progressively as additional signal-processing methods are implemented.
