# Smart Hazard Detector

![Next.js](https://img.shields.io/badge/Next.js-black?logo=next.js)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?logo=firebase&logoColor=black)
![Google Maps](https://img.shields.io/badge/Google%20Maps%20API-4285F4?logo=googlemaps&logoColor=white)

Smart Hazard Detector is a web application that helps drivers identify, report, and visualize road hazards in real time. The platform combines community-reported incidents with interactive mapping to improve road awareness and encourage safer driving.

The application allows users to report hazards, explore nearby incidents on an interactive map, verify community reports, and contribute to a continuously updated hazard database.

## Why this Project?

Road hazards such as potholes, accidents, flooding, and construction zones often go unreported until drivers encounter them. Smart Hazard Detector provides a community-driven platform where users can report, verify, and visualize hazards, helping improve situational awareness and road safety.

**🔗 Live Demo:** [smart-hazard-detector-seven.vercel.app](https://smart-hazard-detector-seven.vercel.app)


> **Note:** The frontend is publicly accessible. Some backend or API-dependent features may require local configuration if backend services are unavailable.

## Screenshots

| Hazard map | Hazard types & severity | Navigation + voice alerts |
|---|---|---|
| ![Hazard map](public/screenshots/01-hazard-map.png) | ![Hazard types and severity](public/screenshots/02-hazard-types-severity.png) | ![Navigation and voice assistance](public/screenshots/03-navigation-voice-assistance.png) |

| Add a hazard | Remove a hazard |
|---|---|
| ![Add hazard](public/screenshots/04-add-hazard.png) | ![Remove hazard](public/screenshots/05-remove-hazard.png) |

## Architecture

![Architecture blueprint](architecture/architecture-blueprint.png)

The main device collects data from the accelerometer, GPS, and elevation change along the z-axis, runs lightweight signal processing to detect a hazard, and pushes it to Firestore. The app reads hazards from Firestore in real time and renders them on a GIS-based map, checking the user's active route against known hazards to trigger proximity alerts.

*(Full workflow diagram: `architecture/workflow-diagram.png`)*

## Features

- 📍 Interactive Google Maps visualization
- 🚧 Report road hazards with location and severity
- 👍 Community verification and validation system
- 🔍 Search and explore nearby hazards
- 🔥 Real-time Firebase database synchronization
- 🔐 Secure user authentication
- 📱 Responsive design for desktop 
- 🎨 Modern user interface built with Tailwind CSS

## Tech Stack

### Frontend
- Next.js
- React
- TypeScript
- Tailwind CSS

### Backend & Database
- Firebase Authentication
- Firebase Firestore
- Python
- Flask

### APIs
- Google Maps JavaScript API
- Google Directions API
- Google Geocoding API


  
## Getting Started

```bash
git clone https://github.com/Harikasan/SmartHazard-Detector
cd SmartHazardDetector
npm install
npm run dev   # http://localhost:3000
```

### Environment variables

Create a `.env.local` file and configure:

```env
NEXT_PUBLIC_GOOGLE_MAP_API_KEY=your_google_maps_api_key
NEXT_PUBLIC_FIREBASE_API_KEY=your_firebase_api_key
NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=your_firebase_auth_domain
NEXT_PUBLIC_FIREBASE_PROJECT_ID=your_firebase_project_id
NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET=your_firebase_storage_bucket
NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=your_firebase_messaging_sender_id
NEXT_PUBLIC_FIREBASE_APP_ID=your_firebase_app_id
ELEVATION_API_KEY=your_google_elevation_api_key
```

- **Firebase:** [Firebase Console](https://console.firebase.google.com/) → create a project → add a Web App → enable Firestore.
- **Google Maps/Directions/Elevation:** [Google Cloud Console](https://console.cloud.google.com/) → enable billing → enable "Maps JavaScript API", "Directions API", "Elevation API" → create a restricted API key.

## Scripts

```bash
npm run dev      # development server
npm run build    # production build
npm run start    # production server
npm run lint     # lint checks
```

## Hazard Types & Severity

**Types:** Pothole · Speed breaker · Manhole
**Severity:** Low · Medium · High

## Future Improvements

- AI-powered hazard severity prediction
- Push notifications for nearby hazards
- Route optimization based on hazard density
- Offline support
- Mobile application
- Administrative dashboard with analytics

