# Algorithmic Trading System

## About
This project was developed as part of the **Software Engineering courses COSC 470 and COSC 471** at Okanagan College. It focused on building an **Algorithmic Trading System (ATS)** capable of collecting, processing, and managing financial market data for analysis with Machine Learning (ML) models.

The project was developed collaboratively using **Agile project management** techniques, following the **SCRUM framework** for iterative development and teamwork. Additionally, **Rational Unified Process (RUP) principles** were applied to structure the project plan, ensuring a well-organized and systematic approach to development.

### Documentation  
As part of the project, extensive documentation was produced to ensure clarity, maintainability, and scalability of the system. This included:
- **System Requirements Specification (SRS)** – Outlining functional and non-functional requirements.  
- **Software Design Document (SDD)** – Detailing system architecture, database schema, and API design.  
- **Project Plan & Sprint Reports** – Tracking Agile development progress, sprint planning, and retrospectives.  
- **User Manual** – Providing instructions on system usage and configuration.  
- **Configuration Management Plan** – Defining version control strategies and deployment procedures. 

Throughout the project, team members gained experience in:
- **Software design and development** using Python and various web technologies.
- **Database design, management and data processing** for financial data analysis.
- **Version control and team collaboration** using Git and Jira.
- **Agile methodologies** with regular sprints, stand-ups, and retrospectives.

The project demonstrated how structured software development practices, along with effective team collaboration, can result in a well-rounded and easily maintainable product.

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

## Contributors
Jacob Rawlings, Jake Fischer, Alan Abdollahzadeh, Benjamin Carrier, Vanessa Dubouzet, Dominic Presch.
