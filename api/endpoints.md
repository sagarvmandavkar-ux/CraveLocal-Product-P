# API Specification: Nashville Street Eats v1

This document outlines the API endpoints required to power the "Nashville Street Eats" feature.

### Base URL
`https://api.cravelocal.com/v1/`

---

### **Get All Vendors**
Returns a list of all active food truck vendors.

* **Endpoint:** `GET /vendors`
* **Query Parameters:**
    * `cuisine` (optional, string): Filters results by cuisine type (e.g., `?cuisine=Tacos`).
    * `min_rating` (optional, float): Filters results for vendors with a rating above the specified value (e.g., `?min_rating=4.7`).
* **Success Response (200 OK):**

```json
[
    {
        "vendor_id": 101,
        "name": "Mas Tacos Por Favor",
        "cuisine": "Tacos",
        "price_range": "$",
        "rating": 4.8,
        "location": {
            "latitude": 36.1764,
            "longitude": -86.7533
        }
    },
    {
        "vendor_id": 102,
        "name": "The Grilled Cheeserie",
        "cuisine": "American",
        "price_range": "$",
        "rating": 4.7,
        "location": {
            "latitude": 36.1499,
            "longitude": -86.8049
        }
    }
]
