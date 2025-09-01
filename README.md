# Weather MCP Server - README

This is a **Python MCP Server** that provides weather data tools (`get_alerts`, `get_forecast`) via the [Model Context Protocol](https://modelcontextprotocol.io/).

---

## 1. Prerequisites

* **Python 3.10+** installed
* [National Weather Service API](https://www.weather.gov/documentation/services-web-api) (no API key required)

---

## 2. Setup

1. **Create & activate virtual environment**

```bash
python -m venv .venv
source .venv/bin/activate  # Linux/Mac
.venv\Scripts\activate    # Windows
```

2. **Install dependencies**

```bash
pip install -r requirements.txt
```

4. **Run MCP server**

```bash
python weather_server.py
```

It should start listening at:

```
http://127.0.0.1:8000
```

---

## 3. Provided Tools

### `get_alerts(state)`

Fetches active weather alerts for a US state.

* **Args:** `state` (string, 2-letter state code)
* **Returns:** Formatted string of alerts

### `get_forecast(latitude, longitude)`

Fetches a 5-period weather forecast for a location.

* **Args:**

  * `latitude` (float)
  * `longitude` (float)
* **Returns:** Formatted forecast string
