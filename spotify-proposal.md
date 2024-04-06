# Spotify Music Dashboard Project Proposal

## Overview

This proposal outlines the development of a personalized music dashboard leveraging the Spotify API. The aim is to enhance users' connection with their favorite music through intuitive features and personalized insights.

## 1. Technology Stack

- **Front-end:** React.js will be used for UI/UX.
- **Back-end:** Node.js will handle API requests and data processing.
- **Database:** PostgreSQL will store user preferences and data for personalized features.

## 2. Project Focus

The project will be a full-stack web application with a focus on both front-end and back-end. 

## 3. Application Type

This will be a web application.

## 4. Project Goal

The goal is to provide a personalized dashboard where users can view their recently played tracks, discover how their music tastes have evolved over time, and create playlists from their personal charts for direct use within the Spotify app.

## 5. User Demographic

The primary users are Spotify users interested in enhancing their listening experience.

## 6. Data Usage and Collection

Data will be sourced from the Spotify API, using the following endpoints:

- **User Profile Data (`GET /v1/me`):** To obtain essential user details such as their Spotify ID, display name, and subscription type. This information will be used for personalizing the dashboard's greeting and for understanding the user's subscription level to tailor features accordingly.

- **Recently Played Tracks (`GET /v1/me/player/recently-played`):** Fetches the user's recently played tracks, providing an overview of their current listening habits. 

- **User's Top Artists and Tracks (`GET /v1/me/top/{type}`):** Determines the user's favorite artists and tracks over time to chart the evolution of the user's music taste over time.

- **Create a Playlist (`POST /v1/users/{user_id}/playlists`):** Enables the creation of new playlists for users directly from the dashboard, and perhaps suggesting personalized playlists.

- **Add Items to a Playlist (`POST /v1/playlists/{playlist_id}/tracks`):** This endpoint is used to populate user-created playlists with recommended tracks or favorites.

User-specific data  will be stored securely in PostgreSQL.

## 7. Project Creation Approach

### a. Database Schema
- **Users:** Store Spotify user IDs, authentication tokens, and app-specific preferences.
- **Playlists:** Record user-created playlists for quick access and modification.
- **Listening History:** Log tracks played for personalized insights and features.

### b. API Challenges
- Handling rate limits and ensuring efficient data fetching without exceeding Spotify API's limitations.
- Maintaining updated and secure authentication tokens for user sessions.

### c. Security
- JWT for session management and secure token storage.
- OAuth 2.0 for Spotify authentication to ensure secure user login.

### d. Functionality
- Visualization of recently played tracks and listening trends over time, perhaps using charts/diagrams.
- Dynamic playlist creation based on user preferences and listening history.
- Personalized music recommendations.

### e. User Flow
- User logs in via Spotify OAuth.
- Dashboard displays recent tracks, personalized insights, and new playlist suggestions.
- Users can create and modify playlists, which sync directly with their Spotify account.

### f. Beyond CRUD
- Incorporates features like real-time data synchronization and Spotify integration, creating a dynamic and interactive iser experience. 
- Stretch goals include developing a mobile app for cross-platform accessibility and adding social media sharing capabilities.

