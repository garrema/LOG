# log-monitoring-system
Project
# Real-Time Log Monitoring & Anomaly Detection System

A backend service that ingests high-volume log streams, normalizes and categorizes them, and automatically surfaces anomalies — built for speed with optimized SQL queries and indexing.

## Overview

In production systems, anomalies buried in thousands of log entries can go undetected for hours. This service automates log ingestion, normalization, and pattern analysis — flagging abnormal behavior in real time so issues can be caught and resolved before they escalate.

## Features

- 📥 **High-volume ingestion** — processes 10,000+ log entries efficiently
- 🕐 **Timestamp normalization** — standardizes log formats across sources for consistent analysis
- 🚨 **Severity categorization** — classifies logs by level (INFO, WARN, ERROR, CRITICAL)
- 🔍 **Anomaly detection** — identifies error spikes and abnormal patterns automatically
- ⚡ **Optimized queries** — SQL indexing strategies for fast retrieval and reduced response times
- 📊 **Traceability** — structured storage enables historical pattern analysis

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Runtime | Node.js |
| Database | PostgreSQL |
| Query Optimization | SQL Indexing |
| Architecture | Backend Service, RESTful API |

## How It Works

```
Raw Log Stream (10K+ entries)
        ↓
  Ingestion Layer (Node.js)
        ↓
  Timestamp Normalization
        ↓
  Severity Categorization
  (INFO / WARN / ERROR / CRITICAL)
        ↓
  PostgreSQL Storage (indexed)
        ↓
  Anomaly Detection Engine
        ↓
  Flagged Alerts + Analytics
```

## Getting Started

```bash
# Clone the repository
git clone https://github.com/garrema/log-monitoring-system.git
cd log-monitoring-system

# Install dependencies
npm install

# Set up environment variables
cp .env.example .env
# Add your PostgreSQL connection string

# Set up the database
psql -U postgres -f schema.sql

# Start the service
npm start
```

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/logs` | Ingest new log entries |
| GET | `/api/logs` | Retrieve logs with filters |
| GET | `/api/anomalies` | View detected anomalies |
| GET | `/api/stats` | Log volume and severity breakdown |

## Performance

- Handles **10,000+ log entries** per ingestion cycle
- SQL indexing reduces query response time significantly
- Normalized schema supports recurring analytical queries without degradation

## Author

**Monish Siddardha Garre** — [LinkedIn](https://www.linkedin.com/in/monish-siddardha-garre-73a897328/) · [GitHub](https://github.com/garrema)
