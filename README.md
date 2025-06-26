# 🔗 URL Shortener with Flask & SQLite

A simple and elegant URL Shortener built using 🐍 Python's Flask framework and SQLite database.

## 📦 Requirements

- Python 3.x
- Flask >= 3.0.0

Install dependencies using:

```bash
pip install -r requirements.txt
````

## 🛠️ How It Works

1. 📝 User inputs a long URL.
2. 🧠 The app stores it in the SQLite database.
3. 🔢 The URL ID is encoded using Base62.
4. 🔗 A short URL is generated and shown.
5. 🚀 Visiting the short URL redirects to the original one.

## 🚀 Running the App

1. 📁 **Clone or download the project** and navigate to the project folder.

2. 📥 **Install the required library**:

   ```bash
   pip install -r requirements.txt
   ```

3. ▶️ **Run the app**:

   ```bash
   python URLShortener.py
   ```

4. 🌐 **Open your browser** and visit:

   ```
   http://127.0.0.1:5000/
   ```

5. 🔗 **Paste a long URL**, hit "Shorten", and you'll get a working short URL!

## 🧪 Example

* Input: `https://www.example.com/some/very/long/url`
* Output: `http://127.0.0.1:5000/abc`

Clicking the short URL will redirect you back to the original.

## 🗃️ Database

SQLite is used to store URLs with the following schema:

```sql
CREATE TABLE IF NOT EXISTS urls (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    url TEXT NOT NULL
);
```

## 🛡️ Error Handling

* Invalid short URLs return a **404**.
* Invalid characters in the short code return a **400**.

## 🧹 Misc

* Ignores `/favicon.ico` requests to avoid noise in logs.

## 🧑‍💻 Author

Made with ❤️ using Flask.

---

Enjoy shortening your URLs! 🔗✨


