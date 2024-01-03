# Rotating-machine-fault-data-set
# Dataset for Machinery Sensor Analysis


## 1.1 Introduction

This database consists of multivariate time series data collected by sensors on SpectraQuest's Mechanical Fault Simulator (MFS) for Calibrated Balance Vibrations (ABVT). It includes two different simulated states: normal operation and imbalance fault.

## 1.2 Data Collection System

### Environmental Monitoring

- **Observe environmental conditions**, including those related to sensors and gateways.
  - Delta Temperature (Sensor – Ambient)
  - Sensor Temperature
  - Ambient Temperature
  - Ambient Humidity

### Trending Analysis

- **Power Band Trending** (from velocity spectrum)
- **Acceleration Root Mean Square (RMS)**
- **Velocity RMS**
- **Crest Factor**
- **Vibration RMS**
- **Acceleration RMS** (All axes)

### Vibration Spectrum

- **Low Res** – Up to 2500Hz/150,000CPM FMax (Each bin = 1.60 Hz)
- **High Res** – Up to 550Hz/33,000CPM FMax (Each bin = 0.34 Hz)

### Time Waveform

- **Low Res Velocity Spectrum** (with Power Bands)
- **Acceleration Spectrum**
- **Displacement Spectrum**

## 1.3 Sequences

Sampling every 3 minutes with the machine running continuously. As vibrations could be induced by noise even when the machine is off, we removed data below the mean value to simulate the machine's on and off states.

- **Normal state**: Original 2200 lines, filtered to 700 lines
- **Imbalance state**: Original 800 lines, filtered to 400 lines
- **Simple Data**：As above, but with mixed features

### Identifiers:

- **N**--Normal
- **Im**--Imbalance
- **S1**--sensor1
- **S2**--sensor2

### Directions:

- **H**--Horizontal
- **V**--Vertical
- **A**--Axial

### Measurement Types:

- **V**--Velocity
- **A**--Acceleration
- **AP**--Acceleration Peak-to-Peak

### Examples:

- **NS1HV**--Normal state sensor 1 Horizontal Velocity
- *Note*: No acceleration data for the horizontal direction

### Data Columns:

A total of 8 columns including AA, AAP, AV, HAP, HV, VA, VAP, VV

## 1.4 Data Size

- **Total**: 11MB
- **Imbalance**: 2.2MB
- **Normal**: 8.2MB
- **Simple version**: 582KB
- **.ipynb file**: 12KB
  
