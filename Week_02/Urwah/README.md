# IMDb Top Movies Scraper #
A Python-based web scraper that extracts data from IMDb's Top 250 movies list using Selenium WebDriver. This project demonstrates advanced web scraping techniques with robust error handling and multiple fallback strategies.

## Project Overview ##
This tool automatically collects comprehensive data about top-rated movies from IMDb, including:

1. Movie titles (properly formatted without ranking numbers)

2. Release years

3. IMDb ratings (numeric values accurately extracted)

4. Poster image URLs (high-quality versions)

The extracted data is saved in a structured CSV format suitable for data analysis, visualization, or archival purposes.

## Features ##
Robust Element Location: Multiple fallback strategies for reliable data extraction

Dynamic Content Handling: Specialized approaches for modern JavaScript-rendered websites

Error Resilience: Comprehensive exception handling with graceful degradation

Resource Management: Proper browser instance handling to prevent conflicts

Data Validation: Quality checks during extraction process

## Technical Stack ##
- Python 3.11+

- Selenium WebDriver - Browser automation

- ChromeDriver - Chrome browser control

- Pandas - Data manipulation and CSV export

- IMDb.com - Data source

## Installation ##
Prerequisites
Python 3.11 or higher

Google Chrome browser

ChromeDriver (matching your Chrome version)

Setup Steps
Clone the repository:

git clone https://github.com/UrwahRasheed80/Week_02/Urwah/imdb_scraper.ipynb
cd imdb_scraper
Install required packages:

Download ChromeDriver (if not included):

Check your Chrome version (chrome://settings/help)

Download matching ChromeDriver from https://chromedriver.chromium.org/

Place chromedriver executable in project directory or add to PATH

## Usage ##
Run the main scraping script:

python imdb_scraper.ipynb
The script will:

Launch a Chrome browser window

Navigate to IMDb's Top 250 movies page

Extract data from the top 100 movies

Save results to movies_data.csv

Close the browser automatically

## Configuration ##
The script includes several configurable parameters:

# Number of movies to scrape
TARGET_COUNT = 100

# Wait times (seconds)
PAGE_LOAD_TIMEOUT = 15
ELEMENT_TIMEOUT = 10

# Output file path
OUTPUT_FILE = "movies_data.csv"
## Technical Implementation ##
Key Techniques Used
Dynamic Waiting Strategy:

WebDriverWait(driver, 15).until(
    EC.presence_of_element_located((By.CSS_SELECTOR, "li.ipc-metadata-list-summary-item"))
)
Multi-Selector Fallback Approach:

year_selectors = [
    "span.sc-b189961a-8",
    "span.cli-title-metadata-item", 
    "ul.ipc-inline-list li:first-child"
]
Attribute-Based Data Extraction:

rating_elem = movie.find_element(By.CSS_SELECTOR, "span.ipc-rating-star")
aria_label = rating_elem.get_attribute("aria-label")
rating = aria_label.split()[2]  # Extract numeric value
Challenges Overcome
Dynamic CSS Classes: IMDb uses randomly generated class names

Attribute-Stored Data: Critical information in non-visible attributes

Resource Conflicts: Browser instance and file handling issues

Website Changes: Adaptive selectors for evolving HTML structures

## Output Format ##
The generated CSV file contains the following columns:

Column	Description	Example
Title	Movie title	"The Shawshank Redemption"
Year	Release year	"1994"
Rating	IMDb rating	"9.3"
Image_URL	Poster image URL	"https://m.media-amazon.com/images/..."
## Contributing ##
Contributions are welcome! Please feel free to submit a Pull Request.

Fork the project

Create your feature branch (git checkout -b feature/AmazingFeature)

Commit your changes (git commit -m 'Add some AmazingFeature')

Push to the branch (git push origin feature/AmazingFeature)

Open a Pull Request

 ## Acknowledgments ##
Data sourced from IMDb

Built with Selenium WebDriver

Inspired by web scraping challenges and solutions

