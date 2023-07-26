# Myntra Product Scraper

![Python](https://img.shields.io/badge/Python-3.7+-blue.svg)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

A straightforward Python script, designed to run in a Jupyter Notebook, that scrapes product data from Myntra.com. The scraper navigates through product listing pages, extracts key details for each item, and organizes the data into separate JSON files for each page scraped.

## Features

-   **Product Data Extraction**: Scrapes essential product information such as name, brand, price, and URL.
-   **Pagination Support**: Automatically navigates through multiple pages of product listings.
-   **Structured Output**: Saves the scraped data in a clean, easy-to-use JSON format.
-   **Page-wise Data**: Generates a separate JSON file for each page, making the data easy to manage and inspect.
-   **Jupyter Notebook Environment**: Encapsulates all code and functions in a single, interactive notebook for ease of use and modification.

## Prerequisites

Before you begin, ensure you have the following installed on your system:
-   [Python](https://www.python.org/downloads/) (version 3.7 or higher)
-   [Jupyter Notebook](https://jupyter.org/install) or JupyterLab
-   Required Python libraries: `requests` and `beautifulsoup4`

## Installation

1.  **Clone the repository:**
    ```sh
    git clone https://github.com/akshay-bharadva/myntra-product-scrapping.git
    cd myntra-product-scrapping
    ```

2.  **Install the required packages:**
    It's recommended to use a virtual environment.
    ```sh
    # Create and activate a virtual environment (optional but recommended)
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`

    # Install dependencies
    pip install requests beautifulsoup4 jupyter
    ```

## Usage

1.  **Launch Jupyter Notebook:**
    Navigate to the project directory in your terminal and run the following command:
    ```sh
    jupyter notebook
    ```
    This will open a new tab in your web browser with the Jupyter interface.

2.  **Open the Notebook:**
    Click on the `.ipynb` file (e.g., `myntra_scraper.ipynb`) to open it.

3.  **Configure the Scraper:**
    Inside the notebook, locate the cell where the target URL is defined. You can modify this URL to point to the specific Myntra product category or search result you wish to scrape.

4.  **Run the Code:**
    Execute the cells in the notebook sequentially. You can do this by selecting a cell and pressing `Shift + Enter` or by using the "Run" button in the toolbar. To run the entire notebook, you can go to `Cell > Run All`.

5.  **Find the Output:**
    As the script runs, it will create `.json` files in the root directory of the project. Each file will be named according to the page number it corresponds to (e.g., `page_1.json`, `page_2.json`, etc.).

## Output Structure

The output for each page is a JSON file containing a list of product objects. Each object follows this structure:

```json
[
  {
    "product_name": "Men Slim Fit Casual Shirt",
    "brand": "HIGHLANDER",
    "price": "₹799",
    "original_price": "₹1099",
    "discount": "(27% OFF)",
    "product_url": "https://www.myntra.com/shirts/highlander/highlander-men-slim-fit-casual-shirt/12345.html"
  },
  {
    "product_name": "Women Solid Running Shoes",
    "brand": "Puma",
    "price": "₹2499",
    "original_price": "₹4999",
    "discount": "(50% OFF)",
    "product_url": "https://www.myntra.com/shoes/puma/puma-women-solid-running-shoes/67890.html"
  }
]
```

## ⚠️ Disclaimer

This script is intended for educational and personal use only. Web scraping can be against the terms of service of some websites. Please ensure you are not violating Myntra's terms of service before using this tool. Be a responsible user: do not send an excessive number of requests in a short period to avoid overloading their servers.

## Contributing

Contributions, issues, and feature requests are welcome. Feel free to check the [issues page](https://github.com/akshay-bharadva/myntra-product-scrapping/issues) if you want to contribute.

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.