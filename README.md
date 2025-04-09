# Algorithmic Trading System

## Overview
The **Algorithmic Trading System (ATS)** is designed to collect and store financial market data for analysis using Machine Learning (ML) models. It automates data gathering from various financial sources, processes the data, and stores it in a structured database.

## Features
- **Automated Data Collection**  
  - Historical and real-time stock, bond, index, and commodity data.  
  - Daily updates for stock ticker symbols and company financials.  
- **Data Management**  
  - Data consistency verification.  
  - Storage in an **OLTP Database** with automated insertion scripts.  
  - Automatic deletion of obsolete data (older than 3 years).  
- **User Interface**  
  - Web-based UI for system configuration and monitoring.  
  - Data export capabilities for research and ML training.  

## System Components
- **Data Collection Scripts:** Fetch financial data from APIs.  
- **OLTP Database:** Stores structured trading data.  
- **Web UI:** User-friendly interface for system configuration and data access.  

## Future Enhancements
- **Data Warehouse Integration** for long-term data storage.  
- **Web Scraping** for additional market insights.  

## Contributors
Jacob Rawlings, Jake Fischer, Alan Abdollahzadeh, Devon Volberg, William Blake, Benjamin Carrier, Vanessa Dubouzet, Dakota Flath, Parker Green, Yuan Hu, Jacob Labelle, Isaac Lengacher-Bergeron, Dominic Presch, Dylan Soares, Jaeden Soukoroff.

## Setup
1. `cp example.env .env`
2. Fill `.env` file with appropriate credentials
   - Can skip this step if only running tests
3. `./setup`
   - Creates the virtual environment and installs necessary packages

## Execution
You can execute scripts using `.venv/bin/python3` as your Python executable.
- `.venv/bin/python3 -m ats.collection.bonds_api_query`

You can also use `source .venv/bin/activate` instead, which is useful when running multiple scripts.
- `source .venv/bin/activate`
- `python3 -m ats.collection.bonds_api_query`
- `python3 -m ats.database.bonds_insert`
- `deactivate`
