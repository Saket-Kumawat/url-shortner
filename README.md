https://url-shortner-5kl4.onrender.com

# 🔗 URL Shortener

A lightweight and performant URL shortening service built using **Golang** for the backend and **HTML + Tailwind CSS** for the frontend.

---

## 📚 Introduction

A URL shortener is a web service that converts long, cumbersome URLs into shorter, more manageable links. These shortened URLs redirect users to the original link, making them ideal for sharing, tracking, and space-saving purposes.

This project demonstrates how to build such a service from scratch using modern web technologies — with an emphasis on simplicity, performance, and clarity.

---

## 🧠 How It Works

1. **User submits a long URL** via the frontend form.
2. The **frontend sends a POST request** to the backend (`/shorten`) with the long URL.
3. The **backend generates a hash-based ID** (first 8 characters of MD5) as the shortened path.
4. The server stores the mapping (in-memory) between the short ID and the original URL.
5. When someone visits `/redirect/{id}`, the backend:
   - Looks up the original URL.
   - Redirects the user using HTTP 302 (Found).

This architecture is intentionally simple and scalable — ideal for learning or prototyping.

---

## ⚙️ Tech Stack

| Layer       | Technology         | Purpose                              |
|-------------|--------------------|--------------------------------------|
| Frontend    | HTML + TailwindCSS | User interface and responsive form   |
| Backend     | Golang (net/http)  | REST API, URL mapping, redirection   |
| Hashing     | MD5 (8 chars)      | Deterministic short URL generation   |
| Storage     | In-memory (map)    | Key-value store for URL mappings     |
| Hosting     | Render             | Free and fast cloud deployment       |

---

## 💡 Why Use Golang?

- 🌐 **Performance**: Go’s native concurrency model and compiled binary structure offer near-native performance.
- 🧩 **Simplicity**: Go's standard library (especially `net/http`) allows for powerful APIs with minimal dependencies.
- 🧪 **Scalability**: Ideal for small services that might scale with minimal infrastructure.

---

## ✨ Features

- 🔗 Shorten any valid HTTP or HTTPS URL
- 🚀 Instant redirection to original URLs
- 🖥️ Responsive frontend UI
- 🧠 Clean and readable Go code
- 🔒 CORS enabled for cross-origin requests
- 📦 Portable and self-contained

---

## 🚀 Deployment Guide (Render.com)

1. **Push to GitHub**:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin https://github.com/your-username/url-shortener.git
   git push -u origin main
