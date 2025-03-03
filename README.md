# Zillow Scraper

This Python module can be used for getting property listings from Zillow. This allows users to extract detailed information about properties available for sale or rent, as well as sold properties, across various states in the USA.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Supported States](#supported-states)
- [Configuration](#configuration)
- [Data Output](#data-output)
- [Logging](#logging)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Features

- Scrape property listings from Zillow for multiple states.
- Retrieve detailed property information including:
  - Address
  - Price
  - Days on Zillow
  - Zestimate and Rent Zestimate
  - Property type (e.g., single-family home, condo)
  - Geographic coordinates (latitude and longitude)
- Support for paginated results, allowing users to scrape multiple pages of listings.

## Installation

To install the Zillow Scraper module, follow these steps:

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/Adeyemi0/zillow_scraper.git
   cd zillow_scraper
   ```


2. **Install the Package:**

   ```bash
   pip install zillow_scraper

   ```

3. **Install Dependencies:**
If you don't have the required libraries, you can install them using:

   ```bash
   pip install -r requirements.txt

   ```
4. **Usage**
To use the Zillow Scraper, you can import the scrape_selected_states function from the module and call it with the desired parameters.

```bash
## Example:

from zillow_scraper.scraper import scrape_selected_states

# Define the states and listing type you want to scrape
selected_states = {
    "California": "ca",
    "Texas": "tx"
}

# Scrape for sale listings
df = scrape_selected_states(selected_states, "for_sale")

# Display the scraped data
print(df.head())

```
## Listing Types:
- for_sale: For properties currently on the market.
- for_rent: For rental listings.
- sold: For properties that have been sold.

## Supported States
The scraper supports all 50 states in the USA. Below is a list of the states and their corresponding abbreviations:
```bash

| State              | Abbreviation |
|--------------------|--------------|
| Alabama            | al           |
| Alaska             | ak           |
| Arizona            | az           |
| Arkansas           | ar           |
| California         | ca           |
| Colorado           | co           |
| Connecticut        | ct           |
| Delaware           | de           |
| Florida            | fl           |
| Georgia            | ga           |
| Hawaii             | hi           |
| Idaho              | id           |
| Illinois           | il           |
| Indiana            | in           |
| Iowa               | ia           |
| Kansas             | ks           |
| Kentucky           | ky           |
| Louisiana          | la           |
| Maine              | me           |
| Maryland           | md           |
| Massachusetts      | ma           |
| Michigan           | mi           |
| Minnesota          | mn           |
| Mississippi        | ms           |
| Missouri           | mo           |
| Montana            | mt           |
| Nebraska           | ne           |
| Nevada             | nv           |
| New Hampshire      | nh           |
| New Jersey         | nj           |
| New Mexico         | nm           |
| New York           | ny           |
| North Carolina     | nc           |
| North Dakota       | nd           |
| Ohio               | oh           |
| Oklahoma           | ok           |
| Oregon             | or           |
| Pennsylvania       | pa           |
| Rhode Island       | ri           |
| South Carolina     | sc           |
| South Dakota       | sd           |
| Tennessee          | tn           |
| Texas              | tx           |
| Utah               | ut           |
| Vermont            | vt           |
| Virginia           | va           |
| Washington         | wa           |
| West Virginia      | wv           |
| Wisconsin          | wi           |
| Wyoming            | wy           |

```
