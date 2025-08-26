# 🎬 GoGO Anime API

The **GoGO Anime API** is your ultimate gateway to a vast anime database.  
Easily fetch information on thousands of anime titles, search by name, filter by genre, and get rich details in a clean JSON format.

👉 [Subscribe on RapidAPI](https://rapidapi.com/naradashen/api/gogo-anime-api)

---

## 🚀 Overview

Unlock the world of anime with the GoGO Anime API, a powerful service perfect for:

- Fan sites and discovery platforms  
- Mobile or web anime apps  
- Recommendation engines  
- Discord/Telegram bots  
- Research or academic projects  

### 🔑 Key Features
- **Detailed Anime Information** → Retrieve synopsis, genres, alternate names, status, and more.  
- **Powerful Search** → Search across title, synopsis, genres, and more.  
- **Genre-Based Discovery** → Fetch anime filtered by genre (e.g., Action, Romance, Isekai).  
- **Developer-Friendly** → RESTful endpoints + JSON responses for easy integration.  
- **Scalable Pricing** → Generous free tier, with higher limits for production use.  

---

## 📌 Endpoints

### 🔹 Get Anime by ID
**Path:** `/api/anime/{id}`  
**Method:** `GET`  
**Example:**  
```http
GET /api/anime/1
```
**Description:** Returns detailed information about a specific anime by its ID.  

---

### 🔹 Search Anime
**Path:** `/api/search?q={query}&field={field}&limit={limit}&page={page}`  
**Method:** `GET`  
**Example:**  
```http
GET /api/search?q=naruto&field=title&limit=10&page=1
```
**Parameters:**  
- `q` → Search query *(required)*  
- `field` → Search field (`title`, `genres`, `other_names`, `synopsis`, `type`, `status`) *(default: title)*  
- `limit` → Results per page *(default: 50, max: 100)*  
- `page` → Page number *(default: 1)*  

---

### 🔹 Get Anime by Genre
**Path:** `/api/genre?genre={genre}&limit={limit}&page={page}`  
**Method:** `GET`  
**Example:**  
```http
GET /api/genre?genre=action&limit=10&page=1
```
**Parameters:**  
- `genre` → Genre name *(required)*  
- `limit` → Results per page *(default: 50, max: 100)*  
- `page` → Page number *(default: 1)*  

---

## 🔑 Authentication

All endpoints require authentication via the **`X-RapidAPI-Key`** header.  

1. Subscribe on [RapidAPI Hub](https://rapidapi.com/naradashen/api/gogo-anime-api).  
2. Get your API key.  
3. Include it in all requests.  

**Example (cURL):**
```bash
curl --request GET   --url "https://gogo-anime-api.p.rapidapi.com/api/anime/1"   --header "x-rapidapi-host: gogo-anime-api.p.rapidapi.com"   --header "x-rapidapi-key: YOUR_API_KEY"
```

---

## 💻 Code Examples

### JavaScript (Node.js)
```javascript
import fetch from "node-fetch";

const url = "https://gogo-anime-api.p.rapidapi.com/api/anime/1";
const options = {
  method: "GET",
  headers: {
    "x-rapidapi-host": "gogo-anime-api.p.rapidapi.com",
    "x-rapidapi-key": "YOUR_API_KEY"
  }
};

fetch(url, options)
  .then(res => res.json())
  .then(data => console.log(data))
  .catch(err => console.error(err));
```

### Python
```python
import requests

url = "https://gogo-anime-api.p.rapidapi.com/api/anime/1"

headers = {
    "x-rapidapi-host": "gogo-anime-api.p.rapidapi.com",
    "x-rapidapi-key": "YOUR_API_KEY"
}

response = requests.get(url, headers=headers)
print(response.json())
```

---

## 📖 Example Response
```json
{
  "success": true,
  "data": {
    "id": 1,
    "title": "0 Years Old Child Starting Dash Story Season 2",
    "image_url": "https://www13.gogoanimes.fi/thumb/1736762631-6480-146764.jpg",
    "type": "TV",
    "plot_summary": "Watch full episodes 0 Years Old Child Starting Dash Story Season 2, download 0 Years Old Child Starting Dash Story Season 2 english subbed, 0 Years Old Child Starting Dash Story Season 2 eng sub, download 0 Years Old Child Starting Dash Story Season 2 eng sub, stream 0 Years Old Child Starting Dash Story Season 2 at 9anime.",
    "released": "January 13, 2025",
    "updated": "May 6, 2025",
    "status": "Ongoing",
    "other_names": "0 Years Old Child Starting Dash Story Season 2, Head Start at Birth Season 2, 0歳児スタートダッシュ物語 シーズン2",
    "genres": [
      "Adventure",
      "Fantasy",
      "Isekai",
      "Reincarnation"
    ],
    "synopsis": "Second season of 0-saiji Start Dash Monogatari.0-saiji Start Dash Monogatari Season 2",
    "movie_id": "1643",
    "default_ep": "0",
    "alias_anime": "0-years-old-child-starting-dash-story-season-2",
    "scraped_at": "2025-08-25T00:35:19.301140"
  }
}
```

---

## 💰 Pricing

- **Free Tier** → Generous monthly requests for testing and hobby projects  
- **Paid Plans** → Higher rate limits for production apps and businesses  

👉 [View Pricing on RapidAPI](https://rapidapi.com/naradashen/api/gogo-anime-api/pricing)

---

## 📬 Support

- RapidAPI → “Contact API Provider”  
- Or open an issue in this GitHub repo  

---

### ⭐ If you like this project, give it a star on GitHub!
