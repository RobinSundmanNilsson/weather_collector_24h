# 🌤️ Weather Collector 24h

## 📖 Description

**Weather Collector 24h** is a Python program that fetches and displays 24-hour weather forecasts from the **SMHI** (Swedish Meteorological and Hydrological Institute) and **YR** (Norwegian Meteorological Institute) APIs.  

Users can choose to retrieve and view forecasts from either or both sources. Forecast data is parsed to display key weather parameters like **temperature** and **precipitation probability**, and is saved as Excel files for easy access and future reference.

---

## ✨ Features

- 🧭 **Interactive Menu**  
  Navigate a simple menu to fetch or display forecasts from SMHI, YR, or both.

- 📍 **Custom Location Input**  
  Retrieve forecasts for any location using latitude and longitude.

- 📊 **Excel Export**  
  Automatically saves forecasts to Excel files for SMHI and YR.

- 🖥️ **Console Display**  
  Outputs a clean, formatted forecast directly in the terminal.

- 🔐 **Secure Config with `constants.py` and `.env`**  
  Sensitive information like headers and user agents are stored securely and never hardcoded.

---

## 🛠️ Requirements

Install the following Python libraries before running the program:

```bash
pip install requests pandas openpyxl python-dotenv
```

If you're using a virtual environment, use the following command:
```bash
uv pip install requests pandas openpyxl python-dotenv
```

The program also uses Python’s built-in `datetime` module.

---

## 🔐 Environment Variables

This program uses a `.env` file to securely store your personal **User-Agent** string required by the YR API.

1. Create a file called `.env` in the root directory.
2. Add your user agent like this:

```env
YR_USER_AGENT="YourCustomUserAgentHere"
```

3. This variable is loaded by the program via `constants.py`, keeping your sensitive info out of the source code.

> ⚠️ **Important:** Make sure `.env` is listed in your `.gitignore` to prevent accidentally committing it.

---

## 🚀 Getting Started

Clone the repository and run the main script:

```bash
python weather_collector_24h.py
```

You'll be prompted to choose which forecast to fetch or view, and enter your desired coordinates.

---

### 🌍 Setting Your Location

When running the program, you’ll be prompted to enter your **latitude** and **longitude**.
Make sure to input coordinates for the location you’d like to get the weather forecast for.

If you press Enter without entering any coordinates, the program will use the default location:

> **Default Location:**  
> 📍 *Liljeholmstorgets Galleria, Stockholm, Sweden*  
> **Latitude:** `59.3084`  
> **Longitude:** `18.0215`

---

## 👤 Intended For

This tool is perfect for users who want a quick, automated way to:
- Check short-term weather forecasts,
- Save data for reference or analysis,
- And do it all from the command line.
