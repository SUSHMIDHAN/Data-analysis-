# Data-analysis-
Nan mudhalvan 
weather_analysis_project/
│
├── data/
│   └── sample_weather_data.csv
│
├── src/
│   ├── __init__.py
│   └── weather_analysis.py
│
└── requirements.txt
Here's the content of `weather_analysis.py`:

```python
import pandas as pd
import matplotlib.pyplot as plt

def load_data(file_path):
    """Load weather data from CSV file."""
    return pd.read_csv(file_path)

def analyze_temperature(data):
    """Analyze temperature trends over time."""
    # Convert 'Date' column to datetime format
    data['Date'] = pd.to_datetime(data['Date'])

    # Plot temperature over time
    plt.figure(figsize=(10, 6))
    plt.plot(data['Date'], data['Temperature'], color='blue')
    plt.title('Temperature Variation Over Time')
    plt.xlabel('Date')
    plt.ylabel('Temperature (°C)')
    plt.grid(True)
    plt.show()

def main():
    # Load data
    file_path = '../data/sample_weather_data.csv'
    weather_data = load_data(file_path)

    # Analyze temperature trends
    analyze_temperature(weather_data)

if __name__ == "__main__":
    main()
```
