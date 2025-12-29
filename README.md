# CS109-Probability-Final-Project
note: moved project over from my old github account. made in Dec 2024 for CS109 course

The project is on probabilistic analysis of classical music through pitch extraction from MIDI files, modeling the distributions of those pitches, and using statistical methods to classify musical segments.

## Project Overview

The goal of this project is to explore how probability and statistics can be used to analyze and classify segments of classical music. By extracting pitch features from MIDI files of pieces by Beethoven and Chopin, I build probabilistic models to study their statistical properties and use these models to classify unknown melody segments.

## Features

- **MIDI Feature Extraction:** Extracts pitch and duration information from MIDI files using Python's `mido` library.
- **Distribution Estimation:** Computes the empirical probability distribution of pitches for each composer using `collections.Counter` for frequency and normal/binomial approximations for density analysis.
- **Visualization:** Provides side-by-side plots of pitch density (histogram and fits) and probability distributions for each composer's piece using Matplotlib.
- **Classification:** Implements log-likelihood comparison to classify new melody segments as resembling either Beethoven or Chopin based on pitch distributions.

## Usage

### Prerequisites

- Python 3.x
- Required packages: `numpy`, `mido`, `matplotlib`, `scipy`

Install dependencies:

```bash
pip install numpy mido matplotlib scipy
```


### Example Output

You will see visualization windows displaying density and probability for each composer. The console will output the classification results for test segments, such as:

```
Segment 1 ([60, 62, 64, 65, 67]) is classified as: Beethoven
...
```

## Project Structure

- `cs109challenge4.py`: Main script for feature extraction, distribution estimation, visualization, and classification.
- `README.md`: Project overview and instructions.
- `pieces/`: Directory for MIDI files (not included).

## Methods

- **extract_features**: Extracts note pitches and durations from a MIDI file.
- **estimate_distribution**: Computes normalized probability for each pitch.
- **plot_density_and_probability**: Visualizes density histogram and probability distribution, including normal/binomial fits.
- **classify_segment**: Classifies a segment using log-likelihood of observed pitches under each composer's pitch distribution.


---

For questions or suggestions, feel free to open an issue in this repository.
