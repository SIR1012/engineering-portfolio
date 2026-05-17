# Webscraper

## Overview

Webscraper is a multi-source scraping and pricing analysis system designed to aggregate product data from multiple external platforms and compare it against internal product data.

The system tracked pricing, product availability, and competitor positioning across approximately 8 external websites.

The primary challenge was not scraping itself, but accurately identifying when products from different websites represented the same underlying item despite inconsistent naming conventions, metadata structures, and formatting.

This project was built before modern AI-assisted development tools became widely available, meaning the matching and normalization systems were implemented using custom logic and heuristics.

---

## My Role

I designed and built the system independently, including:
- scraping workflows
- backend architecture
- database structure
- deployment infrastructure
- normalization systems
- product matching logic
- reliability handling
- scraping infrastructure

The project originally began using FastAPI before later being migrated to Flask as the architecture evolved.

My responsibilities also included:
- maintaining scraping reliability
- handling anti-bot protections
- debugging broken scrapers
- adapting to external website changes
- improving matching accuracy
- maintaining operational stability

---

## Goals

- Aggregate pricing data from multiple competitors
- Track product availability and pricing changes
- Compare external products against internal inventory
- Maintain updated competitive analysis data
- Automate competitor monitoring workflows

---

## Architecture

### Backend
- FastAPI (initially)
- Later migrated to Flask

### Database
- MySQL

### Scraping Infrastructure
- Scrapy
- Selenium

### Deployment
- Self-hosted Nginx server
- Later migrated to Heroku

---

## Core Responsibilities

### Multi-Source Scraping

The system aggregated product data from multiple external websites, each with different structures, layouts, and naming conventions.

### Product Matching

The primary engineering challenge involved determining when products from different websites represented the same underlying item.

### Data Normalization

External product data frequently required normalization before comparison and matching logic could operate reliably.

### Reliability & Maintenance

The system needed to remain operational despite:
- changing website layouts
- inconsistent HTML structures
- blocked requests
- anti-bot protections
- partial failures
- inconsistent external data quality

---

## Key Challenges

### Product Matching

Different websites used:
- inconsistent naming conventions
- different metadata structures
- varying formatting patterns
- incomplete product information
- inconsistent bottle sizing formats
- reordered naming patterns

This made direct string comparison unreliable.

The primary challenge was accurately identifying when products from multiple sources represented the same underlying item while minimizing false matches.

---

### Pre-AI Matching Logic

Since this system was built before modern AI tooling became common, the matching process relied on custom logic and heuristics rather than LLM-based matching systems.

The matching system used combinations of:
- normalized naming patterns
- string similarity comparisons
- metadata weighting
- scoring-based heuristics
- rule-based filtering

to determine likely product matches.

---

### Scraping Reliability

External websites introduced ongoing reliability challenges including:
- blocked requests
- inconsistent layouts
- HTML structure changes
- anti-bot protections
- incomplete responses
- inconsistent page behavior

The scraping infrastructure needed to remain resilient despite unpredictable external systems.

---

### External Data Quality

External product data was often inconsistent or incomplete, requiring preprocessing, cleanup, and validation before comparison logic could operate reliably.

---

## Solutions

### Product Matching System

Built a custom matching system capable of mapping external products against internal database entities while minimizing incorrect matches and false positives.

### Normalization Layer

Introduced preprocessing and normalization stages responsible for standardizing product names, metadata, and formatting prior to comparison.

### Adaptive Scraping Workflow

Implemented scraping workflows capable of adapting to external website changes and handling partial failures gracefully.

### Reliability Handling

Introduced retry logic, validation flows, fallback handling, and defensive scraping strategies to improve operational stability.

---

## What I Learned

This project significantly improved my understanding of:
- entity matching challenges
- normalization systems
- scraping infrastructure
- reliability engineering
- handling inconsistent external data
- anti-bot scraping challenges
- automation-focused backend systems
- operational maintenance of external integrations

---

## What I’d Improve Now

If rebuilding the system today, I would likely:
- introduce more advanced matching/scoring logic
- experiment with AI-assisted entity matching
- improve queue/task orchestration
- improve observability and monitoring
- separate scraping infrastructure more aggressively
- improve scaling and distributed scraping capabilities

---

## Tech Stack

- Python
- JavaScript
- Flask
- FastAPI
- MySQL
- Scrapy
- Selenium
- Nginx
- Heroku
