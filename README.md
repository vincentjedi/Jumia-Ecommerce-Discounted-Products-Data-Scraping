Project Description: Jumia Discounted Product Scraper and Web Interface.

Overview:
This project is a comprehensive solution for scraping discounted product information from Jumia, storing the data in a MySQL database, and providing a user-friendly web interface to display, search, and navigate through discounted products. It integrates web scraping, data processing, database management, and a web application for a seamless experience. The key focus is to allow users to view real-time discounted products ranked by highest discounts and offer links to purchase them directly from Jumia.

Project Components:

1. Web Scraping:

   - Tool Used: Python (with Requests and BeautifulSoup)
   - Description: The scraper collects information from Jumia’s e-commerce site, extracting details such as product name, original price, discounted price, discount percentage, and a direct purchase link for each product. The scraper handles multiple pages of listings and ensures that duplicate products are filtered out, keeping only unique items. The data is saved into a CSV file for further processing.

2. Data Storage:

   - Tool Used: MySQL (with SQLAlchemy and pymysql)
   - Description: The scraped data is stored in a MySQL database, with a table named discountedproducts. The schema includes fields for product name, original price, discounted price, discount percentage, and product URL. SQLAlchemy is used to interact with the database, allowing for efficient querying, inserting, and updating of product data.

3. Data Processing and Automation:

   - Tool Used: Apache Airflow
   - Description: A DAG (Directed Acyclic Graph) in Apache Airflow automates the entire workflow, which includes scraping the product data, saving it to a CSV file, and loading it into the MySQL database. The DAG is scheduled to run daily, ensuring that the database is always up-to-date with the latest product information. Airflow handles task dependencies, error handling, and logging.

4. Web Application:

   - Tool Used: Flask (with Jinja2 templating)
   - Description: The Flask web application acts as the front-end interface. It fetches product data from the MySQL database and displays it dynamically on a web page. The application supports searching for specific products by name, filtering out duplicate entries, and ranking products by the highest discount percentage. Each product also includes an "Order Now" button that links directly to the Jumia product page for easy purchasing.

5. User Interface Enhancements:

   - Tool Used: HTML/CSS (Bootstrap)
   - Description: The UI is designed to be visually appealing and functional. It includes an animated header, a search bar, and a product listing table with pagination controls. Products are displayed with their respective discount percentages, and users can navigate through pages of results with ease. The interface also supports viewing the top-discounted products first.

Key Features:

- Dynamic Data Fetching:

  - Real-time display of discounted products, fetched directly from the database.
  - Search functionality for filtering products by name, with results ranked by discount percentage.
  - Duplicate products are automatically filtered to ensure a clean and concise listing.

- Pagination:

  - Efficient pagination system that displays a set number of products per page.
  - Pagination controls for navigating through large datasets, with "Next", "Previous", "First", and "Last" page options.

- Automated Data Pipeline:

  - The entire scraping and data-loading process is automated with Apache Airflow, ensuring the database is updated daily.
  - Handles large datasets and ensures the system is error-resilient.

- Interactive Web Interface:
  - Built with Flask, the web interface provides an interactive and responsive experience.
  - Users can search, sort, and navigate through discounted products.
  - "Order Now" buttons take users directly to the Jumia website product pages for easy ordering.

Tools Used:

- Python: Core programming language for web scraping, data processing, and automation.
- BeautifulSoup: Library used to parse HTML and extract product details from Jumia.
- Requests: Library for sending HTTP requests to fetch web pages.
- MySQL: Relational database used to store and manage product data.
- SQLAlchemy: ORM (Object-Relational Mapping) tool used to interact with the MySQL database.
- Apache Airflow: Workflow automation tool used to schedule and manage the scraping and data-loading processes.
- Flask: Web framework used to build the web application that displays product data to users.
- HTML/CSS: Technologies used to design and style the web application's interface.

This project integrates multiple technologies to create a reliable and user-friendly system for discovering discounted products on Jumia. It automates the scraping, storage, and display of product data, offering users a seamless way to browse, search, and purchase discounted items. By leveraging automation tools like Apache Airflow and providing a dynamic web interface with Flask, the system remains scalable, efficient, and easy to use.
