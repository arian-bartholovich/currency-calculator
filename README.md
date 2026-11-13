# Currency Calculator

A lightweight web application that combines an expression calculator with live currency conversion. Built with Flask and a responsive browser interface, it demonstrates practical API integration, server-side validation, and asynchronous front-end interactions.

## Overview

Currency Calculator gives users two useful financial utilities in one focused experience: evaluating mathematical expressions and converting amounts between international currencies. The application fetches currency metadata and exchange rates from the Frankfurter API, then returns conversion results through clean JSON endpoints.

## Features

- **Expression calculator** — evaluates arithmetic expressions with addition, subtraction, multiplication, division, and parentheses.
- **Input normalization** — converts display-friendly operators such as `×`, `÷`, and `−` into evaluable expressions.
- **Live currency conversion** — converts an entered amount between selected currencies using current API-supplied rates.
- **Dynamic currency list** — retrieves available currencies from the external service for use in the interface.
- **JSON-based API routes** — supports responsive browser updates without a full page reload.
- **Error-aware backend** — validates required conversion parameters and handles unavailable currency rates.
- **Clean, responsive interface** — provides a familiar calculator layout alongside paired amount and currency fields.

## Technical Highlights

| Area | Implementation |
| --- | --- |
| Backend | Python and Flask |
| External data | Frankfurter currency API |
| HTTP client | Requests |
| Expression evaluation | Asteval interpreter |
| Front end | HTML, CSS, and JavaScript |
| Application design | REST-style JSON endpoints for calculation, conversion, and currency data |

## API Endpoints

| Endpoint | Method | Purpose |
| --- | --- | --- |
| `/` | `GET` | Serves the calculator interface |
| `/calculate` | `POST` | Evaluates an arithmetic expression and returns its result |
| `/convert` | `GET` | Converts an amount between two currency codes |
| `/currencies` | `GET` | Returns available currency codes and names |

## What This Project Demonstrates

- Integrating third-party APIs into a user-facing web product
- Designing clear API contracts with JSON responses
- Validating and normalizing user input on the server
- Connecting a Python backend to interactive JavaScript interfaces
- Building concise, useful tools around a real-world data source
- Handling application errors and edge cases in web routes

## Project Structure

```text
currency-calculator/
├── app.py              # Flask routes, calculation logic, and API integration
├── templates/
│   └── index.html      # Calculator and currency-converter interface
└── static/
    ├── style.css       # Visual styling
    ├── calcScript.js   # Calculator interaction logic
    └── currencyScript.js # Currency-conversion interaction logic
```

## Getting Started

1. Clone the repository and create a Python virtual environment.
2. Install the dependencies:

   ```bash
   pip install flask asteval requests
   ```

3. Start the development server:

   ```bash
   python app.py
   ```

4. Open the local address shown in the terminal, normally `http://127.0.0.1:5000`.

## Author

Developed by **Arian Bartholovich** as a practical Flask project that combines external data integration, interactive front-end development, and clean server-side application logic.
