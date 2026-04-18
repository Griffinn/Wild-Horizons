# 🌍 Wild Horizons API
Wild Horizons is a minimalist yet powerful REST-style API that lets you discover some of the world's most unusual, breathtaking, and mysterious destinations. From glowing caves to forbidden islands, this API is designed for exploration, curiosity, and storytelling. Built using pure Node.js (no frameworks) to showcase strong fundamentals and clean architecture. Instead of generic tourist data, this API focuses on:
* hidden gems 
* natural wonders 
* restricted & mysterious locations 
* surreal landscapes 

# Features
Instead of focusing on overused tourist destinations, it highlights places that are unusual, visually striking, or simply less talked about — the kind of locations that spark curiosity. At the same time, the API is designed to be flexible and practical, so it can be used in real applications like travel planners, discovery platforms, or even storytelling tools.

Some of the key capabilities include:

## Curated global dataset
A thoughtfully selected collection of unique places around the world — from glowing caves and volcanic craters to restricted islands and natural illusions.

## Flexible filtering system
Users can filter destinations based on:
* `country`
* `continent`
* public accessibility (`is_open_to_public`)
This makes it easy to narrow down results depending on travel preferences or constraints.

## Dual filtering approach (Path + Query params)
The API supports both:
* 1. path-based filtering (e.g., `/api/country/india`)
* 2. query-based filtering (e.g., `/api?continent=asia&is_open_to_public=true`)
This combination allows for both simple and more refined searches.

## Fast and lightweight responses
Since the data is locally stored and efficiently filtered, responses are quick and consistent.

## Modular and scalable design
The project is structured in a way that separates:
* data handling
* filtering logic
* response formatting
making it easier to maintain and extend.

## Ready for future expansion
Even though it currently uses static JSON data, the architecture is designed so it can be easily connected to a real database later without major changes.
