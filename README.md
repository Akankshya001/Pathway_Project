# Pathway_Project
A real-time, data-driven dynamic pricing engine for urban parking lots, built for the Summer Analytics 2025 Capstone Project. This repository demonstrates the use of **Pathway**, **Pandas**, **NumPy**, and **Bokeh** to create intelligent, explainable pricing models for city parking spaces using streaming data.

## Table of Contents

- [Overview](#overview)
- [Tech Stack](#tech-stack)
- [Architecture Flow](#architecture-flow)
- [Architecture Diagram](#architecture-diagram)
- [Features](#features)
- [License](#license)

## Overview

This project simulates a real-time dynamic pricing system for 14 urban parking lots using real-world-inspired data streams. The engine ingests streaming data, processes key features in real time, and emits price predictions for each lot, visualized live with Bokeh.

**Key objectives:**
- Real-time dynamic pricing per lot, based on occupancy, queue, traffic, special events, and vehicle type.
- Smooth, explainable price changes.

## Tech Stack

| Component         | Technology               | Purpose                                 |
|-------------------|-------------------------|-----------------------------------------|
| Data Processing   | **Pathway**             | Real-time streaming & windowing         |
| Data Analysis     | **Pandas**, **NumPy**   | Feature engineering, calculations       |
| Visualization     | **Bokeh**               | Real-time interactive plotting          |
| Environment       | **Google Colab**        | Development & demonstration             |
| Version Control   | **Git/GitHub**          | Collaboration & code management         |

## Architecture Flow

1. **Data Ingestion**
   - Simulated real-time data is streamed into the system, preserving timestamp order.
   - Each record includes occupancy, queue length, traffic, special day flag, vehicle type, and lot metadata.

2. **Feature Processing**
   - Pathway processes incoming data in real time, applies windowing (e.g., daily tumbling windows).
   - Features are extracted and aggregated per lot and time window.

3. **Pricing Logic**
   - Pricing models (linear and demand-based) are applied per lot.
   - Demand is calculated using a weighted function of occupancy, queue, traffic, event, and vehicle type.
   - Price is computed, normalized, and clipped for smoothness.

4. **Real-Time Output**
   - Computed prices are emitted per lot and time window.
   - Data is exported to Pandas for visualization.

5. **Visualization**
   - Bokeh displays real-time line plots, one per lot, showing price evolution and facilitating comparison.

## Architecture Diagram
![diagram](https://github.com/user-attachments/assets/88941d0a-c8af-4968-aaba-0d474410b1ab)

## Features

- **Streaming Data**: Handles real-time ingestion and processing.
- **Per-Lot Pricing**: Calculates and updates prices for each lot independently.
- **Multiple Models**: Supports baseline linear, demand-based, and competitive pricing.
- **Explainable Logic**: All price changes are interpretable and bounded.
- **Interactive Visualization**: Live Bokeh plots for each lot.
- **Extensible**: Easily add new features or models.


## License

This project is licensed under the MIT License.
