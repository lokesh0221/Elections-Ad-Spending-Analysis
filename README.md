# Screen Time Analysis with Python

This project analyzes the screen time of users by examining the amount of time spent on different apps, the number of notifications received, and how often apps are opened on a daily basis. The goal is to gain insights into user behavior across different apps.


## Introduction
Screen time analysis refers to the process of evaluating how much time users spend interacting with their devices and various apps. This project demonstrates how to analyze such data using Python, allowing for trends and relationships between screen time, notifications, and app openings to be uncovered.

## Dataset
The dataset used in this project contains the following features:
- `Date`: The date on which the data was recorded.
- `App`: The name of the application being used (e.g., Instagram, WhatsApp).
- `Usage (minutes)`: The total number of minutes spent on the app daily.
- `Notifications`: The number of notifications received from the app each day.
- `Times Opened`: The number of times the app was opened on the recorded day.

## Installation
To run this project locally, you'll need to have Python installed. Follow the steps below to set up the project:

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/screen-time-analysis.git
    cd screen-time-analysis
    ```

2. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

## Usage
Once the project is set up, you can analyze the screen time data with the following steps:

1. Import the necessary Python libraries and load the dataset:
    ```python
    import pandas as pd
    data = pd.read_csv('screentime_analysis.csv')
    ```

2. Perform basic analysis and visualizations, such as trends of screen time across different apps:
    ```python
    import matplotlib.pyplot as plt
    import seaborn as sns
    data['Date'] = pd.to_datetime(data['Date'])
    plt.figure(figsize=(12, 6))
    sns.lineplot(x='Date', y='Usage (minutes)', hue='App', data=data, marker="o")
    plt.title('Screen Time Trends for Different Apps')
    plt.show()
    ```

## Results
Key insights from the screen time analysis include:
- **Instagram** shows the highest screen time usage, with peaks on Mondays, Wednesdays, and Saturdays.
- **Netflix** usage is concentrated mid-week and on weekends.
- **WhatsApp** is frequently opened, particularly on Sundays, with high notification counts.
- A strong correlation between app openings and notifications was observed, suggesting notifications drive app engagement.


---


