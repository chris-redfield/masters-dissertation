# Simulating Sensor Data Collection and Shared Perception for Autonomous Vehicles

This repository contains the documentation for my Master's dissertation project completed at the Universidade de Brasília (UnB) in 2025.

## Project Overview

This research explores the potential of autonomous vehicles (AVs) as mobile sensor platforms to create a virtual infrastructure that supplements traditional Intelligent Transportation System (ITS) data collection methods. The work evaluates the feasibility and impact of collecting and sharing sensor data from autonomous vehicles through simulation experiments using the CARLA and Simu5G frameworks.

## Key Findings

- Adding a dedicated data collection module to vehicles results in minimal system overhead—only 1.1% increased memory usage with direct sensor collection and 2.6% with application performance management tools.
- Network simulations reveal that the bandwidth required for basic V2X communications (61.68 KB/s per vehicle, with low resolution sensor settings) consumes only 0.049% of a 5G antenna's capacity.
- A single 5G antenna could theoretically support over 2000 vehicles simultaneously for basic data sharing.
- Security experiments demonstrate vulnerabilities in V2X systems to spoofing attacks and explore potential countermeasures.

## Repository Structure

- `/data-collection`: Code for AV data collection experiments
- `/traffic-monitoring`: Implementation of traffic monitoring experiments
- `/network-simulation`: CARLA and Simu5G integration for V2X communication tests
- `/security-experiments`: Code for spoofing attack scenarios and detection
- `/drone-simulation`: Drone scenario generation for security testing

## Components

### 1. Data Collection Framework

Evaluates the impact of collecting sensor data on vehicle processing and memory usage. Implements direct sensor collection and APM-based methods.

### 2. Traffic Monitoring Experiment

Demonstrates how collected AV data can be used for real-time traffic monitoring, with experiments in both light and heavy traffic conditions.

### 3. B5GCyberTestV2X Framework

Integration framework between CARLA and Simu5G simulators enabling cooperative perception testing focused on V2X cybersecurity.

### 4. Security Experiments

Simulation of three critical V2X scenarios with spoofing attacks:
- Do Not Pass Warning
- Vulnerable Road User Alerts
- Left Turn Assist

### 5. Vision Model Fine-tuning

Dataset and training code for drone detection as part of a broader attack mitigation strategy.

## Installation & Usage

### Prerequisites
- CARLA Simulator 0.9.13+
- OMNeT++ and Simu5G 
- Python 3.8+
- Required Python packages: carla, numpy, pandas, zmq

### Setup
1. Clone this repository: https://github.com/aassilva/CarlaNetpp
2. Install dependencies: `pip install -r requirements.txt`
3. Configure CARLA simulator path in config files
4. Set up OMNeT++ and Simu5G according to their documentation

### Running Experiments
Refer to individual component directories for specific instructions on running experiments.

## Results

The simulation experiments demonstrate that autonomous vehicles can serve as effective mobile sensor platforms for ITS applications with minimal impact on vehicle resources. The integration between CARLA and Simu5G proves the technical feasibility of real-time data sharing using 5G networks, while security experiments highlight important vulnerabilities that need to be addressed for safe implementation.

## Future Work

- Developing more sophisticated anomaly detection algorithms
- Investigating predictive algorithms for cooperative perception during network disruptions
- Expanding simulation capabilities with realistic moving drone models 
- Hardware-in-the-loop testing with actual vehicle systems

## Author

Christian Moryah Contiero Miranda  
Universidade de Brasília  
Faculdade de Tecnologia  
Departamento de Engenharia Mecânica  

## Advisors

Prof. Dr. João Paulo Javidi da Costa (Advisor)  
Dr. Antonio Silva  
Dr. Daniel Alves da Silva
