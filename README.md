````markdown
# 🛡️ Smart Hazard Detector

<p align="center">
  <img src="public/screenshots/01-hazard-map.png" alt="Smart Hazard Detector" width="900"/>
</p>

<p align="center">
A full-stack web application that enables drivers to detect, report, and visualize road hazards in real time using Google Maps, Firebase, and community-driven reporting.
</p>

<p align="center">

![Next.js](https://img.shields.io/badge/Next.js-black?logo=next.js)
![React](https://img.shields.io/badge/React-20232A?logo=react)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-38B2AC?logo=tailwind-css&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?logo=firebase&logoColor=black)
![Google Maps](https://img.shields.io/badge/Google%20Maps%20API-4285F4?logo=googlemaps&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-black?logo=vercel)

</p>

---

## Overview

Smart Hazard Detector is a full-stack web application designed to improve road safety by enabling drivers to detect, report, and visualize road hazards in real time.

The platform combines community-reported incidents, interactive GIS-based mapping, Firebase real-time synchronization, and Google Maps navigation to help drivers make safer decisions before reaching dangerous road conditions.

Users can report hazards, explore nearby incidents, verify community submissions, and contribute to a continuously updated hazard database.

---

## Why this Project?

Road hazards such as potholes, damaged manholes, flooding, construction zones, and speed breakers often go unnoticed until drivers encounter them.

Smart Hazard Detector provides a community-driven platform where users can report, verify, and visualize hazards in real time, improving situational awareness while promoting safer roads through collaborative reporting.

---

## Live Demo

🔗 **Frontend Demo**

https://smart-hazard-detector-seven.vercel.app

> **Note:** The frontend is publicly accessible. Some backend services or API-dependent features may require local configuration if backend services are unavailable.

---

# Project Highlights

- 🚧 Community-driven road hazard reporting
- 🗺️ Interactive GIS visualization using Google Maps
- 🔥 Real-time synchronization with Firebase Firestore
- 📍 Route-aware hazard visualization
- 📱 Fully responsive interface
- ⚡ Built with modern full-stack technologies
- ☁️ Cloud deployment using Vercel

---

# Screenshots

## Hazard Map

![Hazard Map](public/screenshots/01-hazard-map.png)

---

## Hazard Types & Severity

![Hazard Types](public/screenshots/02-hazard-types-severity.png)

---

## Navigation & Voice Assistance

![Navigation](public/screenshots/03-navigation-voice-assistance.png)

---

## Add Hazard

![Add Hazard](public/screenshots/04-add-hazard.png)

---

## Remove Hazard

![Remove Hazard](public/screenshots/05-remove-hazard.png)

---

# Architecture

![Architecture Blueprint](architecture/architecture-blueprint.png)

The application continuously collects hazard-related information through user reports and location services. Hazard information is processed and stored in Firebase Firestore, enabling real-time synchronization across connected clients.

Google Maps APIs provide interactive visualization, route calculation, and location services, allowing the application to compare a user's navigation path with reported hazards and generate proximity-based alerts.

The architecture is designed to support scalable cloud synchronization while maintaining responsive client-side performance.

**Additional Workflow Diagram**

```
architecture/workflow-diagram.png
```

---

# System Architecture

```text
              User
               │
               ▼
    Next.js + React Frontend
               │
        ┌──────┴──────┐
        ▼             ▼
    Firestore    Google Maps APIs
        │             │
        └──────┬──────┘
               ▼
      Real-Time Hazard Reporting &
        Route-Based Visualization
```

---

# Features

- 📍 Interactive Google Maps visualization
- 🚧 Report hazards with GPS location
- 🔥 Real-time Firebase synchronization
- 👍 Community hazard verification
- 🔍 Search nearby hazards
- 🚗 Route-aware hazard visualization
- 🧭 Google Maps navigation integration
- 📱 Responsive desktop experience
- 🎨 Modern UI built using Tailwind CSS

---


# Tech Stack

| Category          | Technologies                                                             |
| ----------------- | ------------------------------------------------------------------------ |
| Frontend          | Next.js, React, TypeScript, Tailwind CSS                                 |
| Backend Services  | Firebase Firestore                                                       |
| Database          | Firebase Firestore                                                       |
| Maps & Navigation | Google Maps JavaScript API, Directions API, Elevation API                |
| Deployment        | Vercel                                                                   |


---

# Project Structure

```text
SmartHazard-Detector/
│
├── app/
├── architecture/
├── components/
├── hooks/
├── lib/
├── public/
│   └── screenshots/
├── styles/
├── package.json
├── next.config.mjs
└── README.md
```

---

# Getting Started

Clone the repository

```bash
git clone https://github.com/Harikasan/SmartHazard-Detector.git
```

Move into the project

```bash
cd SmartHazard-Detector
```

Install dependencies

```bash
npm install
```

Run the development server

```bash
npm run dev
```

Open

```
http://localhost:3000
```

---

# Environment Variables

Create a `.env.local` file.

```env
NEXT_PUBLIC_GOOGLE_MAP_API_KEY=

NEXT_PUBLIC_FIREBASE_API_KEY=

NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=

NEXT_PUBLIC_FIREBASE_PROJECT_ID=

NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET=

NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=

NEXT_PUBLIC_FIREBASE_APP_ID=

ELEVATION_API_KEY=
```

### Firebase

Create a Firebase project and enable:

- Firestore Database

### Google Cloud

Enable the following APIs:

- Maps JavaScript API
- Directions API
- Elevation API

Generate a restricted API key and configure it inside `.env.local`.

---

# Available Scripts

| Command | Description |
|----------|-------------|
| `npm run dev` | Start development server |
| `npm run build` | Build production application |
| `npm run start` | Run production build |
| `npm run lint` | Run lint checks |

---

# Hazard Categories

| Hazard Type | Severity Levels |
|--------------|----------------|
| Pothole | Low • Medium • High |
| Speed Breaker | Low • Medium • High |
| Manhole | Low • Medium • High |

---

# Future Improvements

- AI-powered hazard severity prediction
- Automatic hazard detection using mobile sensors
- Push notifications for nearby hazards
- Offline reporting support
- Mobile application
- Analytics dashboard
- Heatmap visualization
- Administrative moderation panel
- Machine learning–based hazard classification
- Multi-language support

---

# License

This project is licensed under the [MIT License](LICENSE).

---

````
