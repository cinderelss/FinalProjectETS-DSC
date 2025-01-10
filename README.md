# Gait Phase Detection Using Neural Networks

This project implements a neural network to detect gait phases based on Force Sensing Resistor (FSR) data. The system identifies specific phases of the gait cycle, such as Initial Contact (IC), Heel Off (HO), Flat Foot (FF), Toe Off (TO), Mid-Stance (Mst), and Swing.

## Overview
Gait analysis is a critical component in the assessment of human movement and is widely used in healthcare, sports, and rehabilitation. This project trains a feedforward neural network to predict gait phases from FSR data collected from heel and toe sensors.

### Key Features
- Two-layer neural network (input-to-hidden and hidden-to-output).
- Custom backpropagation algorithm for training.
- Visualization of the detected gait phases.

## How It Works

### Data Preprocessing
- The training dataset (`training_project1.dat`) and testing dataset (`recall_project1.dat`) are loaded using Pandas.
- Threshold-based conditions classify heel and toe sensor data into IC, HO, FF, and TO events.

### Neural Network Architecture
1. **Input Layer:**
   - Two neurons (heel and toe sensor data).
2. **Hidden Layer:**
   - Twelve neurons.
3. **Output Layer:**
   - Six neurons (IC, HO, FF, TO, Mst, Swing).

### Training Process
- **Weight Initialization:**
  Random weights and biases for input-to-hidden and hidden-to-output layers.
- **Activation Function:**
  Sigmoid function.
- **Loss Function:**
  Mean Squared Error (MSE).
- **Learning Rate:**
  Dynamic learning rate decreases with iterations.
- **Backpropagation:**
  Gradients are calculated to adjust weights and biases for minimizing error.

### Prediction
After training, the model predicts gait phases from the test dataset (`recall_project1.dat`).

### Visualizing Gait Phases
The script generates bar plots for:
1. Gait phases during training.
2. Predicted gait phases on test data.

Example visualization:
- Blue: Heel sensor data.
- Red: Toe sensor data.
- Green: Mid-Stance (Mst).
- Orange: Initial Contact (IC).
- Black: Heel Off (HO).
- Yellow: Flat Foot (FF).
- Purple: Toe Off (TO).
- Yellow: Swing phase.

### Output Predictions
Predictions are saved in the test dataset (`recall_project1.dat`) with added columns:
- `IC`: Initial Contact
- `HO`: Heel Off
- `FF`: Flat Foot
- `TO`: Toe Off
- `Mst`: Mid-Stance
- `Swing`: Swing phase

## Output
The model outputs:
1. Plots showing sensor data and detected gait phases.
2. Updated test dataset with detected phases.
