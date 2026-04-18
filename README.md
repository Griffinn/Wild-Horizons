# Wild Horizons API
Wild Horizons is an API built for curious travelers who want to go beyond the usual tourist spots. Instead of the same crowded landmarks, it helps you discover unique, lesser-known places across the world — from glowing caves and surreal landscapes to remote islands and hidden natural wonders.
<br>
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)
![Status](https://img.shields.io/badge/Status-Maintained-brightgreen?style=for-the-badge)
![Category](https://img.shields.io/badge/Travel-Discovery-orange?style=for-the-badge)
![Architecture](https://img.shields.io/badge/Architecture-Modular-7C4DFF?style=for-the-badge)
![Data](https://img.shields.io/badge/Data-JSON-00ACC1?style=for-the-badge)
![License](https://img.shields.io/badge/License-ISC-1976D2?style=for-the-badge)
![Backend](https://img.shields.io/badge/Pure_Node-B19CD9?style=for-the-badge&logo=node.js&logoColor=white)
![Code](https://img.shields.io/badge/Logic-AEC6CF?style=for-the-badge&logo=javascript&logoColor=white)
![Design](https://img.shields.io/badge/Biophilic_Vibes-77DD77?style=for-the-badge&logo=leaf&logoColor=white)
![Fun](https://img.shields.io/badge/Hidden_Gems-FFB7B2?style=for-the-badge&logo=sparkles&logoColor=white)
<br>
![Tech](https://img.shields.io/badge/Built_with_Love-C71585?style=for-the-badge&logo=node.js&logoColor=white)
![Style](https://img.shields.io/badge/Aesthetic-API-DB7093?style=for-the-badge&logo=github)
![Nature](https://img.shields.io/badge/Green_Tech-2E8B57?style=for-the-badge&logo=tree)
![Status](https://img.shields.io/badge/Status-Sparkling-FF69B4?style=for-the-badge&logo=star)

![Door To Hell,Darvaza,Turkmenistan](assets/DoorToHell.png)

## Project Overview
Wild Horizons is a minimalist yet powerful REST-style API that lets you discover some of the world's most unusual, breathtaking, and mysterious destinations. From glowing caves to forbidden islands, this API is designed for exploration, curiosity, and storytelling. Built using pure Node.js (no frameworks) to showcase strong fundamentals and clean architecture. Instead of generic tourist data, this API focuses on:
* hidden gems 
* natural wonders 
* restricted & mysterious locations 
* surreal landscapes 

## ⚙️ Features
Instead of focusing on overused tourist destinations, it highlights places that are unusual, visually striking, or simply less talked about — the kind of locations that spark curiosity. At the same time, the API is designed to be flexible and practical, so it can be used in real applications like travel planners, discovery platforms, or even storytelling tools.

Some of the key capabilities include:

* **1. Curated global dataset:**
A thoughtfully selected collection of unique places around the world — from glowing caves and volcanic craters to restricted islands and natural illusions.

* **2. Flexible filtering system:** 
Users can filter destinations based on:
  * `country`
  * `continent`
  * public accessibility (`is_open_to_public`)
This makes it easy to narrow down results depending on travel preferences or constraints.

* **3. Dual filtering approach (Path + Query params):**
The API supports both:
  * 1. path-based filtering (e.g., `/api/country/india`)
  * 2. query-based filtering (e.g., `/api?continent=asia&is_open_to_public=true`)
This combination allows for both simple and more refined searches.

* **4. Fast and lightweight responses:**
Since the data is locally stored and efficiently filtered, responses are quick and consistent.

* **5. Modular and scalable design:**
The project is structured in a way that separates:
  * data handling
  * filtering logic
  * response formatting
making it easier to maintain and extend.

* **6. Ready for future expansion**
Even though it currently uses static JSON data, the architecture is designed so it can be easily connected to a real database later without major changes.

## 🛠️ Tech Stack

The project uses a minimal but purposeful tech stack, focusing on understanding core backend concepts rather than relying on heavy frameworks. At its heart, Wild Horizons is built using Node.js with the native HTTP module, which means everything — from routing to response handling — is implemented manually. This gives deeper insight into how APIs actually work under the hood. Here’s a closer look at the stack:

* **Node.js (Core HTTP Module):** Used to create the server and handle incoming requests and responses without external frameworks like Express. This keeps the project lightweight and closer to the fundamentals.
* **ES Modules:** The codebase uses ES module syntax (import/export), helping keep files organized and the structure clean and maintainable.
* **JSON:** A static JSON dataset is used to store destination information. It acts as a simple stand-in for a database while keeping development straightforward.
* **Custom utility functions:** Instead of relying on libraries, filtering and response handling are implemented through custom utilities, which:
   * improve reusability
   * keep logic modular
   * make the code easier to understand and extend
* **Abstracted data layer:** A small database abstraction (getDataFromDB) is included so that the current JSON-based setup can later be replaced with a real database like MongoDB or PostgreSQL with minimal changes.

## 📦 Installation & Setup

Getting the API up and running locally is straightforward. Since the project uses only Node.js core modules, there are no heavy dependencies to worry about.

**1. Clone the repository:** 
 ```bash
git clone https://github.com/Griffinn/Wild-Horizons.git
cd wild-horizons
```

**2. Install dependencies:** <br><br>
Even though the project is lightweight, it’s good practice to install dependencies:
 ```bash
npm install
```

**3. Start the server:** 
 ```bash
npm start
```

**4. Access the API:** <br><br>
Once the server is running, you can access it at:
 ```bash
http://localhost:8000
```
You can test endpoints directly in your browser or use tools like Postman.

## 💡 API Endpoints
The Wild Horizons API provides a simple and flexible way to explore destinations using both **path parameters** and **query parameters**.

### 1. Get All Destinations (with optional filters):
This endpoint returns all destinations by default. You can optionally apply filters using query parameters.
```bash
GET /api
```
This endpoint returns all destinations by default. You can optionally apply filters using query parameters.

#### Example:
```bash
/api?continent=asia&is_open_to_public=true
```

####  Supported Query Parameters:

| Parameter            | Type    | Description                                  |
|---------------------|--------|----------------------------------------------|
| `continent`           | string | Filter by continent (e.g., asia, europe)     |
| `country`           | string | Filter by country (e.g., india, usa)         |
| `is_open_to_public`   | boolean | Filter by accessibility (true / false)       |

You can combine multiple parameters to refine your results.

---

### 2. Filter by Continent
```bash
GET /api/continent/:continent
```
Returns all destinations within a specific continent.

#### Example:
```bash
/api/continent/asia
```

---

### 3. Filter by Country
```bash
GET /api/country/:country
```
Returns all destinations within a specific country.

#### Example:
```bash
/api/country/india
```

---

### 4. Invalid Routes
Any route that does not match the above patterns will return:
```json
{
  "error": "not found",
  "message": "The requested route does not exist"
}
```


### Example Response
```json
[
  {
    "name": "Magnetic Hill",
    "location": "Ladakh",
    "country": "India",
    "continent": "Asia",
    "is_open_to_public": true,
    "details": [
      {
        "fun_fact": "Vehicles appear to roll uphill due to an optical illusion."
      },
      {
        "description": "A perplexing stretch of road in the Himalayas where gravity seemingly takes a puzzling turn."
      }
    ],
    "uuid": "550e8400-e29b-41d4-a716-446655440015"
  }
]
```

## Project Structure
```text
wild-horizons/
│
├── data/
│   └── data.js              # Static dataset
│
├── database/
│   └── db.js               # Data access abstraction
│
├── utils/
│   ├── getDataByPathParams.js
│   ├── getDataByQueryParams.js
│   └── sendJSONResponse.js
│
├── server.js               # Core server & routing logic
├── package.json
```

## Architecture Overview

The project follows a modular structure:

* `Data Layer` → static JSON dataset
* `Database Layer` → abstraction (getDataFromDB)
* `Utility Layer` → reusable filtering functions
* `Server Layer` → request handling and routing

This makes it easy to:

* swap JSON → real database later
* extend filtering logic
* scale routes cleanly

#### Data Flow:
`Client Request` → `Server (Route Handling)` → `Database Layer (getDataFromDB)` → `Filtering Logic (Path / Query)` → `Response Utility (sendJSONResponse)` → `Client Response (JSON)`

## Future Improvements
* Add endpoint: `/api/:uuid`
* Sorting (`?sort=name`)
* Pagination (`?limit=5`)
* Integrate a real database (MongoDB / PostgreSQL)
* Smarter filtering (multiple values, ranges)






