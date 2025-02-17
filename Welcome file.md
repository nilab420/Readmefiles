# FastAPI Web Scraper

## Overview
This project is a FastAPI-based web scraping service that extracts product information from e-commerce websites using Selenium, ZenRows, and LangChain. It fetches, cleans, and processes HTML content to extract structured product details.

## Features
- Fetch HTML content using **Selenium** and **ZenRows API**.
- Clean HTML by removing unnecessary elements.
- Convert cleaned HTML into markdown for better readability.
- Extract product details using **LangChain** and process responses with **BM25 retrieval**.
- FastAPI endpoints to trigger and retrieve product information.

## Installation

### Prerequisites
Make sure you have the following installed:
- Python 3.8+
- pip (Python package manager)

### Setup
1. Clone the repository:
   ```sh
   git clone https://github.com/your-repo/web-scraper-fastapi.git
   cd web-scraper-fastapi
   ```
2. Create and activate a virtual environment:
   ```sh
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```
3. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```
4. Create a `.env` file for API keys:
   ```sh
   touch .env
   ```
   Add the following variables:
   ```env
   ZENROWS_API_KEY=your_zenrows_api_key
   LANGCHAIN_API_KEY=your_langchain_api_key
   SERPER_API_KEY=your_serper_api_key
   ```

## Usage

### Running the API
Start the FastAPI server with:
```sh
uvicorn main:app --reload
```

### API Endpoints

#### 1. Fetch Product Details
**Endpoint:** `POST /scrape`

**Request Body:**
```json
{
  "query": "Apple iPhone 15 Pro Max (256 GB)",
}
```

**Response:**
```json
  {
        "product_name": "Apple iPhone 15 Pro Max (256 GB) - Natural Titanium",
        "price": 5345.84,
        "currency": "SAR",
        "source": "https://www.amazon.sa/-/en/Apple-iPhone-Pro-Max-256/dp/B0CHXSKYN6",
        "vat_status": null,
        "payment_type": null
  }
```

## Contributing
Feel free to fork the repo, submit issues, or create pull requests!

## License
This project is licensed under the MIT License.

