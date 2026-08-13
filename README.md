# SDN Traffic Recognition with Artificial Neural Networks

An SDN-based network traffic recognition system that applies artificial neural networks to network traffic classification.

This project was developed as part of a master's thesis and integrates **Software-Defined Networking (SDN)**, **artificial neural networks**, and **deep learning** to build a network traffic recognition system.

## Overview

Traditional network traffic identification often relies on predefined rules or port-based classification. However, modern network applications and encrypted traffic make these approaches increasingly challenging.

This project explores the use of machine learning and neural networks for network traffic recognition in an SDN environment.

The system combines:

* **Software-Defined Networking (SDN)**
* **Ryu SDN Controller**
* **Mininet**
* **OpenFlow**
* **Artificial Neural Networks**
* **TensorFlow / Keras**
* **Python**
* **MongoDB**

The overall architecture is designed to collect network traffic information, extract relevant features, perform classification using a trained neural network, and analyze the recognition results.

## System Architecture

The experimental environment is based on an SDN architecture consisting of:

```text
                    ┌─────────────────────┐
                    │    SDN Controller   │
                    │        Ryu          │
                    └──────────┬──────────┘
                               │
                         OpenFlow
                               │
                    ┌──────────▼──────────┐
                    │    OpenFlow Switch   │
                    └───────┬─────┬───────┘
                            │     │
                       ┌────▼─┐ ┌─▼────┐
                       │ Host │ │ Host │
                       └──────┘ └──────┘
                            │
                       Network Traffic
                            │
                    ┌───────▼────────┐
                    │ Traffic Feature │
                    │   Extraction    │
                    └───────┬────────┘
                            │
                    ┌───────▼────────┐
                    │ Neural Network │
                    │  Classification│
                    └───────┬────────┘
                            │
                    ┌───────▼────────┐
                    │ Recognition /  │
                    │    Analysis    │
                    └────────────────┘
```

## Features

* SDN-based network traffic monitoring
* Network traffic feature collection and processing
* Neural network-based traffic classification
* Integration with Ryu SDN Controller
* Network topology and traffic simulation using Mininet
* Deep learning model training using TensorFlow and Keras
* Traffic classification result analysis
* Classification performance evaluation using confusion matrices
* MongoDB-based data storage and management

## Technologies

| Category             | Technology |
| -------------------- | ---------- |
| Programming Language | Python     |
| SDN Controller       | Ryu        |
| Network Emulator     | Mininet    |
| Network Protocol     | OpenFlow   |
| Machine Learning     | TensorFlow |
| Deep Learning        | Keras      |
| Database             | MongoDB    |
| Network Environment  | SDN        |

## Machine Learning

The project uses artificial neural networks to identify different types of network traffic.

The training pipeline can be summarized as:

```text
Network Traffic
      │
      ▼
Feature Collection
      │
      ▼
Data Preprocessing
      │
      ▼
Training Dataset
      │
      ▼
Neural Network
      │
      ▼
Traffic Classification
      │
      ▼
Evaluation
```

The classification performance can be evaluated using metrics such as:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix

## Experimental Environment

The network environment is constructed using **Mininet**, while **Ryu** is used as the SDN controller.

This allows the project to create a controllable SDN environment for generating and analyzing different network traffic patterns.

A typical environment consists of:

```text
Mininet
   │
   ├── Host
   ├── Host
   └── OpenFlow Switch
             │
             ▼
        Ryu Controller
```

## Results

The system evaluates the performance of the trained neural network by comparing the predicted traffic classes with their actual labels.

The confusion matrix provides an overview of the classification performance across different traffic categories and helps identify classes that are difficult for the model to distinguish.

## Project Structure

The project structure may be organized as follows:

```text
.
├── README.md
├── controller/
│   └── ryu/
├── network/
│   └── mininet/
├── dataset/
├── model/
├── training/
├── evaluation/
└── requirements.txt
```

> The directory structure may vary depending on the implementation and experimental environment.

## Installation

Clone the repository:

```bash
git clone https://github.com/<your-username>/sdn-traffic-recognition-ann.git
cd sdn-traffic-recognition-ann
```

Install the required Python packages:

```bash
pip install -r requirements.txt
```

Make sure the required SDN and network simulation environments are installed:

* Ryu
* Mininet
* OpenFlow-compatible switch environment
* Python
* TensorFlow
* Keras
* MongoDB

## Usage

### 1. Start the SDN Controller

Start the Ryu controller application:

```bash
ryu-manager <controller_application>.py
```

### 2. Start the Mininet Environment

Create the experimental network topology:

```bash
sudo mn --controller=remote
```

The exact topology and parameters depend on the experimental configuration.

### 3. Generate Network Traffic

Generate network traffic between Mininet hosts and collect the corresponding traffic information.

### 4. Train the Model

Prepare the dataset and run the training process:

```bash
python <training_script>.py
```

### 5. Evaluate the Model

Evaluate the trained model using the test dataset:

```bash
python <evaluation_script>.py
```

## Research Purpose

The main purpose of this project is to investigate whether artificial neural networks can be applied to network traffic recognition in an SDN environment.

By combining centralized SDN network management with machine learning-based traffic classification, the system provides a foundation for future research in:

* Intelligent network management
* Network traffic classification
* SDN security
* Network anomaly detection
* AI-assisted network monitoring
* Intelligent network services

## Thesis

This project is based on the master's thesis:

> **軟體定義網路基於人工神經網路之流量辨識系統設計**

English title:

> **A Traffic Recognition Based on Artificial Neural Networks in SDN Systems**

## Author

**Janice**

Master's Thesis Project
Taipei Tech University

## License

This project is provided for academic and research purposes.

Please contact the author before using, modifying, or redistributing the project for commercial purposes.
