# 🌐 HTTP (HyperText Transfer Protocol)

---

# 📌 What is HTTP?

HTTP (HyperText Transfer Protocol) is the communication protocol that allows a web browser and a web server to exchange information through requests and responses.

Simply put,

👉 HTTP is the language used by browsers and websites to communicate.

---

# 🤔 Why was HTTP created?

Computers and web servers need a common language to communicate.

HTTP defines rules for sending requests and receiving responses so that every browser can communicate with every website in the same way.

---

# ⚙️ How HTTP Works

Step 1:
You type a website URL.

↓

Step 2:
Your browser sends an HTTP Request.

↓

Step 3:
The server receives the request.

↓

Step 4:
The server processes it.

↓

Step 5:
The server sends back an HTTP Response.

↓

Step 6:
Your browser displays the webpage.

---

# 📤 HTTP Request

A Request is a message sent by the browser to the server asking for something.

Examples:

- Open homepage
- Login
- Search products
- Download image

---

# 📥 HTTP Response

A Response is the server's reply to the browser.

The response may contain:

- HTML
- CSS
- JavaScript
- Images
- JSON Data
- Status Code

---

# 📦 HTTP Headers

Headers are extra information sent along with every request and response.

They tell the server things like:

- Which browser is being used?
- Which language is preferred?
- Is the user logged in?
- What type of data is expected?

Think of headers like the address label on a courier package.

Without the address, the package doesn't know where to go.

---

# 🚀 Common HTTP Methods

## GET

Purpose:
Retrieve information.

Example:
Opening Google homepage.

Example URL:

GET /index.html

---

## POST

Purpose:
Send new data to the server.

Example:
Logging into Instagram.

---

## PUT

Purpose:
Update existing data.

Example:
Updating your profile picture.

---

## DELETE

Purpose:
Delete existing data.

Example:
Deleting an email.

---

# 📊 Common HTTP Status Codes

200 → OK (Success)

201 → Created

301 → Moved Permanently

302 → Redirect

400 → Bad Request

401 → Unauthorized

403 → Forbidden

404 → Not Found

500 → Internal Server Error

503 → Service Unavailable

---

# 🍕 Real Life Example

Imagine ordering pizza.

You → Customer

Waiter → HTTP

Kitchen → Server

Pizza → Response

You tell the waiter:

"I want one Margherita Pizza."

↓

The waiter carries your request.

↓

The kitchen prepares it.

↓

The waiter brings the pizza back.

That's exactly how HTTP works.

---

# 💼 Interview Explanation (30 Seconds)

HTTP stands for HyperText Transfer Protocol.

It is an application-layer protocol that allows communication between clients (browsers) and servers using a request-response model.

The browser sends an HTTP request, the server processes it, and returns an HTTP response containing data like HTML, JSON, images, or status codes.

---

# 🔬 Observe in Burp Suite

While looking at HTTP History, try finding:

✅ Request Method

✅ Host

✅ Path

✅ User-Agent

✅ Accept

✅ Cookie

✅ Response Status

---

# 📝 Questions I Still Have

- Why do websites use HTTPS instead of HTTP?
- What exactly is a Cookie?
- Why are Headers important?
- What is HTTP/2?