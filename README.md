# User Action Propensity Scoring

An educational project developed as part of the **ITMO ML System Design course**.

The goal is to design a scalable ML system that predicts the probability of users performing target actions in a digital product.

## Project Overview

The system aims to provide a unified approach to generating **user propensity scores** for various actions, such as searching, clicking, booking, or saving items.

These predictions can support multiple use cases:

- **Marketing:** audience selection for personalized campaigns.
- **Product:** personalization of user experience.
- **Customer Support:** identification of users who may benefit from proactive assistance.
- **Analytics:** behavioral analysis and user segmentation.

## ML Problem

The task is formulated as supervised binary classification.

For each user, target action, and prediction date, the model estimates the probability of performing that action within a future time window (e.g., 7, 14, or 30 days).

The system is designed to:

- Support multiple target actions and prediction horizons.
- Regularly update propensity scores using historical user behavior.
- Make predictions available to downstream systems.
- Allow new target actions to be added.
- Monitor model quality and prediction stability.

The initial scope focuses on **batch inference**, without real-time predictions or causal effect estimation.

## Technology Stack

- **Python 3.12** — programming language.
- **uv** — dependency and environment management.
- **Ruff** — linting and formatting.
- **pre-commit** — automated code quality checks.

The ML and data processing stack will be defined during system development.

## Getting Started

### Installation

Clone the repository:

```bash
git clone https://github.com/aspnmrv/itmo_mlsd.git
cd itmo_mlsd
```

Install dependencies and Git hooks:

```bash
uv sync
uv run pre-commit install
```

### Code Quality

Run the linter:

```bash
uv run ruff check .
```

Format Python code:

```bash
uv run ruff format .
```

Run pre-commit checks:

```bash
uv run pre-commit run --all-files
```

## Documentation

Detailed system design documentation, including requirements, data pipelines, modeling, architecture, and monitoring, will be maintained in the `docs/` directory.

## Project Status

**In development** — system design and initial project setup.