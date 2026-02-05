# Landmark Detection & Tracking

A small educational project demonstrating robot motion, landmark creation, and sensing in a 2D grid world. The notebooks and helper code show how noisy motion and measurements affect localization and provide the foundation for exploring SLAM (Simultaneous Localization and Mapping) concepts.

## Contents

- `robot-moving-and-sensing.ipynb` — Interactive notebook demonstrating the `robot` class, movement, landmark creation, sensing, and example data collection.
- `landmark-detection-and-tracking.ipynb` — (Related notebook) additional experiments and tracking code.
- `robot_class.py` — standalone robot class implementation
- `helpers.py` — Utility functions used for visualization in the notebooks

## Project overview

The core is a `robot` class that models:

- Pose (`x`, `y`) in a square world
- Motion with Gaussian-like noise
- Measurement/sensing of landmarks with limited range and measurement noise
- Random landmark generation

The notebooks guide you through creating a world, moving the robot, generating landmarks, and collecting measurement + motion data in a time-series format suitable for building or testing SLAM algorithms.

## Requirements

- Python 3.8+
- NumPy
- Matplotlib

Install dependencies with pip:

```
pip install numpy matplotlib
```

## Usage

1. Open `robot-moving-and-sensing.ipynb` in Jupyter or VS Code and run the cells sequentially.
2. Inspect the `robot` class, call `make_landmarks`, `move`, and `sense` to collect `measurements` and `data` used for SLAM-style exercises.
3. Use `display_world` from `helpers.py` to visualize the robot and landmarks.

## Notes and next steps

- The code is intended for learning and experimentation rather than production. You can extend it by adding odometry models, probabilistic filtering (particle or Kalman filters), or a complete SLAM backend that ingests the generated `data` sequence.

## Acknowledgments

This project was completed as part of the Udacity Computer Vision Nanodegree Program.