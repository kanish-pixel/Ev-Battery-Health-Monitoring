# AI-Assisted Battery Degradation Aware Smart EV Charging System

## Project Overview

This project proposes an intelligent EV charging system that monitors battery voltage, current, and temperature to estimate battery health and automatically select an appropriate charging mode.

## Objectives

* Monitor battery parameters in real time.
* Estimate battery State of Health (SoH).
* Identify healthy and aged batteries.
* Reduce battery degradation.
* Improve charging safety.

## Hardware Components

* ESP32
* INA219 Current Sensor
* DS18B20 Temperature Sensor
* Voltage Sensor
* MOSFET
* LM2596 Buck Converter
* 2S BMS
* Lithium-Ion Battery Pack
* LEDs

## Working Principle

1. Read battery voltage, current, and temperature.
2. Calculate battery health.
3. Classify battery as healthy or aged.
4. Select charging mode:

   * Healthy → Fast Charging
   * Aged → Slow Charging
5. Monitor temperature continuously.
6. Stop charging if temperature exceeds the safety limit.

## Battery Health Classification

| SoH (%) | Status   | Charging Mode       |
| ------- | -------- | ------------------- |
| > 90    | Healthy  | Fast Charging       |
| 70–90   | Moderate | Controlled Charging |
| < 70    | Aged     | Slow Charging       |

## Temperature Protection

| Temperature | Action          |
| ----------- | --------------- |
| < 40°C      | Normal Charging |
| 40–50°C     | Warning         |
| > 50°C      | Stop Charging   |

## Results

### Temperature Reduction

| System          | Temperature |
| --------------- | ----------- |
| Existing System | 55°C        |
| Proposed System | 42°C        |

### Degradation Reduction

The proposed charging system reduces battery degradation by adapting charging speed according to battery health.

## Future Scope

* Machine Learning-Based SoH Prediction
* Mobile Application Integration
* Cloud Monitoring
* EV Charging Station Deployment


