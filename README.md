# weather_api.py
import requests

API_KEY = "c84faf0165d8d98e8f6a48c9767f9007"
BASE_URL = "https://api.openweathermap.org/data/2.5/weather"

city = input("Enter city name: ").strip()

params = {
    "q": city,
    "appid": API_KEY,
    "units": "metric"
}

response = requests.get(BASE_URL, params=params)

print("Status Code:", response.status_code)
print("Raw Response:", response.text)
