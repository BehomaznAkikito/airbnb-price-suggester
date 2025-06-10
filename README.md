🏡 Airbnb Price Suggester

This repository contains a Python script that helps Airbnb hosts dynamically calculate appropriate prices for vacant dates. If you've ever felt that Airbnb's Smart Pricing undercuts your revenue or ignores your local context, this tool is designed for you.

✨ What This Tool Does

This script suggests nightly prices for your vacant dates, based on:

Your calendar data (via iCal export)

Your base price and minimum price settings

Day-of-week modifiers (e.g. weekends can be priced higher)

Currency conversion (USD or any other)

Optional manual discounting based on occupancy trends

It's fully editable and intended to be modified to suit your own strategy.

🧪 Why This Exists

If you turn on Airbnb's Smart Pricing, your listing can get undervalued quickly. This tool was created after experiencing repeated drops in occupancy and revenue due to automated pricing algorithms that weren't transparent or host-friendly.

As a host, I wanted:

To manually control my minimum pricing thresholds

To distinguish between weekday and weekend pricing

To offer longer-stay discounts when appropriate

To see all prices in advance, exported to a readable CSV file

This tool offers that transparency and autonomy.

🔧 Requirements

Python 3.9+

An iCal URL for your Airbnb listing(s)

An Open Exchange Rates API key (for currency conversion)

Install dependencies:

pip install -r requirements.txt

🏡 How to Get Your Airbnb iCal URL

Open your Airbnb Hosting Dashboard

Click on a listing to enter the individual calendar view (not the multi-calendar)

Click the “Settings” (⚙️) icon or the three-dot menu in the calendar view

Choose “Export calendar”

Copy the iCal URL, which should look like this:

https://www.airbnb.com/calendar/ical/xxxxxxxx.ics?s=YYYYYYYY

Paste it into the script like this (removing the #):

ical_urls = [
  "https://www.airbnb.com/calendar/ical/xxxxxxxx.ics?s=YYYYYYYY",
  "https://www.airbnb.com/calendar/ical/zzzzzzzz.ics?s=WWWWWWWW",
]

Repeat for each of your listings.

🌐 How to Get Your Exchange Rate API Key

Sign up for a free plan at openexchangerates.org

Get your App ID

In your terminal, set the key like this before running the script:

export OXR_APP_ID="your_api_key_here"

▶️ How to Run

Once you've updated the URLs and exported your API key:

python pricing_suggestion.py

A CSV file will be generated in the current directory, e.g.:

pricing_suggestion_202507.csv

📌 License

MIT License. Use, share, modify freely.

😋 Author

Developed by @BehomaznAkikito to help fellow Airbnb hosts escape the black box of Smart Pricing and reclaim control over their listings.

Feedback and suggestions are welcome!
