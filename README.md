# Wild Horizons API
Wild Horizons is an API built for curious travelers who want to go beyond the usual tourist spots. Instead of the same crowded landmarks, it helps you discover unique, lesser-known places across the world — from glowing caves and surreal landscapes to remote islands and hidden natural wonders.

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
git clone https://github.com/your-username/wild-horizons.git
cd wild-horizons
```

**2. Install dependencies:** <br>
Even though the project is lightweight, it’s good practice to install dependencies:
 ```bash
npm install
```

**3. Start the server:** 
 ```bash
npm start
```

**4. Access the API:** <br>
Once the server is running, you can access it at:
 ```bash
http://localhost:8000
```
You can test endpoints directly in your browser or use tools like Postman.


