# 🛒 Amazon Price Tracker Web Scraper

This project is a Python-based web scraper that monitors the price of a specific Amazon product and notifies the user when the price drops below a certain threshold. It utilizes `BeautifulSoup`, `requests`, and `smtplib` to collect, store, and act on product data.

---

## 📌 Project Overview

This script performs the following:

- Connects to an Amazon product page
- Extracts the product title and current price
- Cleans and structures the data
- Appends daily data to a CSV for trend tracking
- Sends an email notification if the price falls below a user-defined threshold

---

## 🧠 What I Learned

- Web scraping techniques using `BeautifulSoup` and `requests`
- HTML parsing and tag targeting
- Data cleaning and manipulation in Python
- File handling and CSV writing/reading
- Automating tasks using loops and `time.sleep()`
- Sending emails with `smtplib`
- Writing functions for modular code reuse

---

## 🧪 Tech Stack

- 🐍 Python
- 🧼 BeautifulSoup
- 🌐 Requests
- 📅 datetime
- 📤 smtplib (Email)
- 📊 CSV & pandas

---

## 📂 Project Structure
```pgsql
📦 amazon-price-tracker/
┣ 📄 amazon_price_tracker.py
┣ 📄 AmazonWebScraperDataset.csv
┣ 📄 README.md
```

- `amazon_price_tracker.py`: Main script with scraping, email logic, and scheduler
- `AmazonWebScraperDataset.csv`: Log file with product price and date
- `README.md`: Project documentation

---

## 🚀 How It Works

1. **Scraping**  
   Accesses the Amazon product page using `requests` with a user-agent header to mimic a browser.

2. **Parsing HTML**  
   Uses `BeautifulSoup` to find:
   - `productTitle` → product name
   - `priceblock_ourprice` → product price

3. **Data Logging**  
   Cleans the data and appends to a CSV file for future use.

4. **Email Notification** *(optional)*  
   When a price drop condition is met, it sends an email using `smtplib`.

5. **Automation**  
   The `while(True)` loop checks the price once every 24 hours (`86400` seconds).

---

## 📧 Email Notification Logic

```python
if float(price) < 15:
    send_mail()
```
✉️ Email is sent through Gmail SMTP on price trigger.
🔒 Note: Credentials must be secured (avoid hardcoding in production).

## 📸 Sample Output:
```text 
Funny Got Data MIS Data Systems Business Analyst T-Shirt
16.99
2021-08-21
```
### CSV structure:
```javascript
Title,Price,Date
Funny Got Data MIS Data Systems Business Analyst T-Shirt,16.99,2021-08-21
```

⚠️ Disclaimer
Amazon pages often change structure and use anti-bot protections. This scraper may stop working or get blocked. Use responsibly and sparingly. 
Consider using Amazon’s Product Advertising API for a more reliable approach.

## 🔗 Resources

- 📘 [BeautifulSoup Documentation](https://www.crummy.com/software/BeautifulSoup/bs4/doc/)
- 🌐 [Requests Documentation](https://docs.python-requests.org/en/latest/)
- 📤 [smtplib (Python Email Docs)](https://docs.python.org/3/library/smtplib.html)
- 📊 [Pandas Library](https://pandas.pydata.org/docs/)
- 🧼 [CSV File Handling in Python](https://docs.python.org/3/library/csv.html)
- 🧠 [Real Python - Web Scraping with Python](https://realpython.com/web-scraping-with-python/)
- 🔒 [How to Store Sensitive Info (env vars)](https://12factor.net/config)
- 📑 [HTML Element Reference - MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)

---

## 🛠️ Future Improvements

- Track multiple products across different URLs
- Set user-defined price thresholds dynamically
- Add GUI or dashboard (using Tkinter or Streamlit)
- Schedule with cron jobs or cloud functions (AWS Lambda, GCP Cloud Scheduler)
- Add notification via SMS using Twilio
- Store data in SQLite or PostgreSQL instead of CSV
- Use environment variables for secure email credentials
- Visualize price trends using `matplotlib` or `seaborn`
- Error logging and retry mechanism for failed requests

---

## 📬 Contact

**Sefa The Analyst**  
📧 [sefabckn@gmail.com](mailto:sefabckn@gmail.com)  
💼 [LinkedIn (optional)](https://www.linkedin.com)  
🐍 Python | Data Analytics | Automation Enthusiast

