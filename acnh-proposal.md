# Animal Crossing Companion App Project Proposal

## Overview

This proposal details the creation of a companion app for Animal Crossing: New Horizons players. Utilizing the Animal Crossing: New Horizons API, the app aims to help players of the Animal Crossing: New Horizons game on the Nintendo Switch to track their collection of critters (bugs, fish, and deep-sea creatures), fossils, and art pieces. Users can check off items as they collect them, mark them as donated to the museum, and provide real-time suggestions towards completing their collections. 

## 1. Technology Stack

- **Front-end:** React.js will be used for UI/UX.
- **Back-end:** Node.js will handle API requests and data processing.
- **Database:** PostgreSQL for storing user data and collections.


## 2. Project Focus

The project will be a full-stack web application with a focus on both front-end and back-end. 

## 3. Application Type

This will initially be developed as a web application, with plans to adapt it into a mobile app to enable push notifications related to critter availability and other timely events.

## 4. Project Goal

This app aims to help players of the Animal Crossing: New Horizons game on the Nintendo Switch to track their collection of critters (bugs, fish, and deep-sea creatures), fossils, and art pieces. Users can check off items as they collect them, mark them as donated to the museum, and provide real-time suggestions towards completing their collections. 

## 5. User Demographic

Animal Crossing: New Horizons players of all ages looking for an easy way to track progress towards their in-game achievements. It caters especially to players aiming to complete their museum collections and keep track of their critter captures.

## 6. Data Usage and Collection

The app will utilize data from the Animal Crossing: New Horizons API for information on critters, fossils, and art pieces. User inputs and collection status will be stored in PostgreSQL.

## 7. Project Creation Approach

### a. Database Schema
- **Users:** To store account information and authentication details.
- **Collections:** Records of critters, fossils, and art pieces, including whether they have been collected and donated.
- **Notifications:** User preferences for receiving push notifications about critter availability.

### b. API Challenges
- Ensuring the app respects the rate limits and terms of use of the Animal Crossing API.
- Implementing efficient data synchronization to reflect possible updates in API structure.
- This API does not require authentication, which simplifies access but I'll need to manage data privacy and security on my end.

### c. Security
- JWTs for secure user authentication

### d. Functionality
- Interactive checklists for tracking collections of critters, fossils, and art pieces.
- Functionality to mark items as donated to the museum.
- Personalized notifications for critter availability based on user location and time.

### e. User Flow
- Upon login, users would be presented with their collection dashboard which would include critters available to catch on this day/time.
- Users can browse categories (critters, fossils, art) and check off items as collected/donated.
- Museum tab, which offers categories and lists of all items donated to the museum, as well as what has yet to be donated.
- Users set preferences for push notifications for critter availability.

### f. Beyond CRUD
- Features that make this more than a CRUD map are the real-time notifications, data visualization, and social sharing (desired future state).
- Stretch goals involve localization and implementing multiple languages, to accomodate users across available regions, plus a mobile app version. Perhaps also integration with social media - to post about celebrating milestones (such as donating all fish to the museum).

