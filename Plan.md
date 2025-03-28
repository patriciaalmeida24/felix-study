# Step-by-Step Plan
1. Preprocessing
  -	Preprocessing:
    -	Filter: 0.5–50 Hz bandpass to remove noise (e.g., 60 Hz interference).
    -	Artifact Removal: Use ICA to clean out blinks, muscle twitches, etc.
    -	Proposed Segmentation: Divide into 2-second epochs (300 total, or ~600 with 50% overlap) for stable PSD estimates.
    -	Quality Check: Reject epochs with noisy data
2. Power Spectral Density (PSD) Calculation
  -	Purpose: Quantify power in bands (delta: 1–4 Hz, theta: 4–8 Hz, alpha: 8–12 Hz, beta: 13–30 Hz, gamma: 30–50 Hz) during rest.
  -	Windowing: choose a windowing technique
  -	Method: Apply FFT to each epoch, average PSDs across all clean epochs per patient.
  -	Output: PSD values (µV²/Hz) per band, capturing resting-state power (e.g., high theta, low alpha).

3. FOOOF Analysis
  -	Purpose: Decompose PSD into periodic and aperiodic components for precise metrics.
  -	Tool: FOOOF Python package.
  -	Steps:
    1.	Fit FOOOF to averaged PSD (1–40 Hz range).
    2.	Extract:
      -	Center Frequency (CF): Peak frequency per band.
      -	Exponent: Aperiodic slope (steep = slower brain).
      -	Offset: Aperiodic baseline power.
        ○	Band Focus: Delta, theta, alpha, beta .
  -	Output: FOOOF parameters per patient (e.g., theta CF, exponent).

4. Subgrouping MDD Patients
  -	Clustering:
    1.	 Features: FOOOF parameters (CFs, exponent, offset).
      -	Center frequency (e.g. exact gamma peak at 39, 40 or 41 Hz)
      -	Peak power for the different frequency bands
      -	Bandwith
    2.	Method: K-means clustering (test 2–4 clusters).
    3.	Optimize: Use elbow method or silhouette score.
  -	Validation: Compare PSD band power (e.g., theta, alpha) across clusters.
  -	Output: Subgroups (e.g., high-theta/steep-exponent vs. low-alpha/flat-exponent).
  - Subgrouping Impact: Cluster based on these (e.g., k-means with theta power, gamma power, exponent).
