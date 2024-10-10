# Nairabet Web Scraping

The **Nairabet Web Scraping** script is designed to scrape upcoming football match data from the Nairabet website. The script extracts match details such as the match time, teams, and betting odds (home, draw, away) and saves them in a CSV file for further analysis or integration into betting strategies.

## 📌 Features

- **Automated Data Scraping**: Collects football match data and odds from the Nairabet site.
- **CSV Output**: Organizes and stores the scraped data in a CSV file for easy access.
- **Duplicate and Exception Handling**: Ensures data is clean by removing rows with invalid odds and handling potential duplicates.
- **Dynamic Page Loading**: Automatically clicks the "View More" button to load additional matches.

## 🚀 How It Works

1. **Initialization**: A headless browser session is created using Selenium, and the script navigates to the Nairabet football page.
2. **Page Interaction**: The script interacts with the "View More" button multiple times to load additional matches from the site.
3. **Data Scraping**: Extracts match details (time, home and away teams, and odds for each match).
4. **CSV Storage**: Stores the collected data in a CSV file at a specified path.
5. **Data Cleaning**: Invalid rows (with non-numeric odds) are automatically removed from the CSV file.

### Key Components:

- **Selenium**: Used to automate interactions with the Nairabet website, including clicking and scrolling.
- **BeautifulSoup**: Extracts match information from the page's HTML content.
- **CSV File Management**: Manages saving the match data into CSV files and ensuring data integrity through duplicate removal and exception handling.

## 🛠️ Requirements

Make sure to have the following dependencies installed:

- **Python 3.x**
- **Selenium**
- **BeautifulSoup**
- **Pandas**

Install the required dependencies using pip:
```bash
pip install selenium beautifulsoup4 pandas
```

## 🏃 How to Run the Script

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/Ezee-Kits/Nairabet-Scraping.git
   ```

2. **Set Up ChromeDriver**:  
   Download and install [ChromeDriver](https://sites.google.com/a/chromium.org/chromedriver/) to match your Chrome version, and ensure it's in your system path.

3. **Run the Python Script**:
   ```bash
   python nairabet_scraper.py
   ```

4. **View Results**:  
   The scraped data will be saved in the `NAIRABET.csv` file in the specified directory.

## 📁 CSV Output

The CSV file will contain the following columns:
- **TIME**: The time of the match.
- **HOME TEAM**: The home team’s name.
- **AWAY TEAM**: The away team’s name.
- **HOME ODD**: Odds for the home team to win.
- **DRAW ODD**: Odds for a draw.
- **AWAY ODD**: Odds for the away team to win.
- **BOOKMAKER**: Always set to "NAIRABET" for this scraper.

## 🔧 Future Enhancements

- **Real-Time Updates**: Add real-time updates to scrape new matches as they are added.
- **Error Handling**: Enhance error handling for unexpected website changes.
- **Multi-Sport Support**: Extend the script to scrape other sports in addition to football.

## 📝 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## 🤝 Contributing

Contributions are welcome! Please feel free to open issues, suggest improvements, or submit pull requests.
