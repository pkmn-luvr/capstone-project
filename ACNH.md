# Animal Crossing New Horizon's Companion App

## Table of Contents
- [API Endpoints](#api-endpoints)
  - [Fossils](#fossils)
  - [Art](#art)
  - [Fish](#fish)
  - [Deep Sea Creatures](#deep-sea-creatures)
  - [Bugs](#bugs)
- [App Outline](#app-outline)
  - [Initial Setup](#initial-setup)
  - [Directory Structure](#directory-structure)
    - [Front-end Structure](#front-end-structure)
    - [Back-end Structure (Node.js)](#back-end-structure-nodejs)
  - [Development Approach](#development-approach)
  - [Starting Development](#starting-development)
  - [Schema Design](#schema-design)
- [Schema](#schema)

## API Endpoints

### Fossils
- Individual Fossil: `https://api.nookipedia.com/nh/fossils/individuals/{fossil}`
- All Fossils: `https://api.nookipedia.com/nh/fossils/individuals`
  - Fields:
    - Name
    - Image_url
    - Url to Nookipedia

### Art
- Individual Artwork: `https://api.nookipedia.com/nh/art/{artwork}`
- All Artwork: `https://api.nookipedia.com/nh/art`
  - Fields:
    - Name
    - Image_url
    - Url to Nookipedia

### Fish
- All Fish: `https://api.nookipedia.com/nh/fish`
- Individual Fish: `https://api.nookipedia.com/nh/fish/{fish}`
  - Fields:
    - Name
    - Image_url
    - Url to Nookipedia
    - Rarity
    - North Hemisphere availability array
    - South Hemisphere availability array

### Deep Sea Creatures
- All Sea Creatures: `https://api.nookipedia.com/nh/sea`
- Individual Sea Creature: `https://api.nookipedia.com/nh/sea/{sea_creature}`
  - Fields:
    - Name
    - Image_url
    - Url to Nookipedia
    - Rarity
    - North Hemisphere availability array
    - South Hemisphere availability array

### Bugs
- All Bugs: `https://api.nookipedia.com/nh/bugs`
- Individual Bug: `https://api.nookipedia.com/nh/bugs/{bug}`
  - Fields:
    - Name
    - Image_url
    - Url to Nookipedia
    - Rarity
    - North Hemisphere availability array
    - South Hemisphere availability array


## App Outline

### Initial Setup
- **Start with Create React App**
  - Run `npx create-react-app acnh-companion-app`

#### Front-end Structure
- **Components**: Create components for displaying the different types of data (fossils, art, fish, deep-sea creatures, and bugs).
- **Pages**: Implement pages that will be routed to.
- **Services**: Handle API calls in a separate services directory.

#### Back-end Structure (Node.js)
- **Server Setup**: Set up Express server.
- **Routes**: Define routes and implement controllers to handle the logic for each route.
- **Models**: Define models for database schemas.

### Development Approach
- **Dynamic vs. Static**: Use a combination of dynamic and interactive elements with static routing for the best user experience.
- **React Router**: Use for routing to different pages of the app.
- **UX Considerations**: Incorporate loading states and feedback for user actions.

### Starting Development
- **Front-end**: Lay out React components and set up routes.
- **Back-end**: Set up a basic Express server and establish the database connection.
- **Integrate API**: Fetch and display data dynamically from the Nookipedia API.

### Schema Design
- **Users**
  - `id`: Primary Key
  - `username`: String
  - `email`: String
  - `passwordHash`: String
  - `createdAt`: DateTime
  - `updatedAt`: DateTime
- **Collections**
  - `id`: Primary Key
  - `userId`: Foreign Key (References Users)
  - `itemType`: String (e.g., "Fossil", "Fish")
  - `itemName`: String
  - `collected`: Boolean
  - `donated`: Boolean
  - `createdAt`: DateTime
  - `updatedAt`: DateTime
- **Notifications**
  - `id`: Primary Key
  - `userId`: Foreign Key (References Users)
  - `type`: String (e.g., "Critter Available")
  - `message`: String
  - `createdAt`: DateTime
  - `updatedAt`: DateTime

## Directory Structure

```plaintext
acnh-companion-app/
├── client/
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   │   ├── common/
│   │   │   │   ├── Header.js
│   │   │   │   ├── Footer.js
│   │   │   │   ├── LoadingSpinner.js
│   │   │   │   ├── ErrorBoundary.js
│   │   │   │   ├── SearchBar.js
│   │   │   │   ├── CustomButton.js
│   │   │   │   ├── Icon.js
│   │   │   │   └── ToolTip.js
│   │   │   ├── collection/
│   │   │   │   ├── CollectionItem.js
│   │   │   │   ├── FilterOptions.js
│   │   │   │   ├── AvailabilityIndicator.js
│   │   │   │   └── CollectionOverview.js
│   │   │   ├── user/
│   │   │   │   ├── UserProfile.js
│   │   │   │   └── NotificationBell.js
│   │   │   ├── DetailModal.js
│   │   │   └── ...
│   │   ├── pages/
│   │   │   ├── HomePage.js      // Landing Page/Dashboard - Consider modals for featured items?
│   │   │   ├── LoginPage.js
│   │   │   ├── RegisterPage.js
│   │   │   ├── CrittersPage.js     // Critters Overview - Filters like hemisphere availability
│   │   │   ├── FossilsPage.js
│   │   │   ├── ArtsPage.js
│   │   │   ├── FishesPage.js
│   │   │   ├── SeaCreaturesPage.js
│   │   │   ├── BugsPage.js
│   │   │   ├── CollectionTrackerPage.js
│   │   │   ├── UserProfilePage.js
│   │   │   ├── AboutPage.js
│   │   │   ├── FAQPage.js           // maybe, maybe not
│   │   │   ├── ContactPage.js
│   │   │   └── ...
│   │   ├── services/
│   │   │   └── apiService.js
│   │   ├── App.js
│   │   └── index.js
│   └── package.json
├── server/
│   ├── config/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   │   ├── index.js
│   │   └── users.js
│   ├── utils/
│   ├── app.js
│   └── package.json
└── README.md
