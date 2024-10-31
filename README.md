
# GitHub Users and Repositories in Chennai

- **Data scraping process:** This project uses the GitHub API to fetch details about GitHub users in Chennai with over 50 followers and their repositories, including metadata and repository statistics.
- **Interesting insight:** The most surprising insight was the diversity of companies represented, including startups and multinational corporations, with high activity in languages like Python and JavaScript.
- **Developer recommendation:** Consistently updating and documenting repositories, especially with popular languages, increases the likelihood of engagement and followers on GitHub.

## Project Overview

This project involved scraping GitHub data using the GitHub API, focusing on users in Chennai with more than 50 followers. The data collected comtains details on user profiles and up to 500 of their public repositories. The data was saved into `users.csv` and `repositories.csv`, maintaining the original API format as required.

## Files Included

1. **`users.csv`:** Contains user details such as username, full name, company, city, email, hiring status, and other key information.
2. **`repositories.csv`:** Contains repository details including repository name, creation date, star count, watchers count, language, and license information.
3. **`README.md`:** Provides an overview of the project, insights, and a developer recommendation.
4. **Code files:** The Python scripts used for data scraping and cleaning are included for transparency and reproducibility.

## Data Collection Process

The data collection process involves several functions:
- `get_users_in_chennai()`: Finds GitHub users in Chennai with over 50 followers.
- `get_user_details()`: Fetches detailed information for each user, including cleaning the company names.
- `get_user_repositories()`: Retrieves up to 500 public repositories per user, including important repository metadata.

**Note:** Rate limiting on GitHub's API is managed by using a token and a retry mechanism, with a delay between requests to prevent hitting rate limits.

## How to Run

### Run on colab

   1. Open the "GithubAPI_datascraper.ipynb"(https://colab.research.google.com) in Google Colab. 
   2. Replace with your personal GitHub API token in the notebook to authenticate your requests.
   3. Run each cell to scrape the data and save the outputs (`users.csv` and `repositories.csv`) to your Google Drive or download them directly.

### Run locally

1. **Install Dependencies:** Ensure you have `pandas` and `requests` installed.
   ```bash
   pip install pandas requests
   ```

2. **Run the Script:** Execute the main script, which fetches data and saves it to `users.csv` and `repositories.csv`.
   Make sure to Replace "GITHUB TOKEN" with your personal taken

   ```bash
   python github_scraper.py
   ```

3. **View the Files:** Open `users.csv` and `repositories.csv` for user and repository data.

## Analysis Highlights

- **Active Languages:** High activity was found in languages like Python and JavaScript, suggesting a strong developer community focus in these areas.
- **Company Presence:** The data shows a mix of local and global companies, with users representing well-known tech firms and innovative startups.
- **Recommendations:** Developers seeking visibility on GitHub should focus on maintaining updated repositories, using popular programming languages, and regularly engaging with followers.
