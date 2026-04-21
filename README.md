# JoinIn 

> **The "Just-in-Time" Connection Layer for the SRM AP Campus.**
> *Built for the Code For Connection (Web/Mobile Development) Hackathon.*

---

## 🎯 The Problem & Solution

**The Context:** Students at SRM AP are surrounded by thousands of peers but often eat alone, study alone, or struggle to find teammates due to the high social friction of asking, "Can I join you?"

**The Solution:** JoinIn bridges this gap by allowing students to broadcast temporary "Beacons" of intent (e.g., "Studying C++ @ Library"). Peers can view the live radar and instantly join these beacons, breaking the ice before they even meet.

---

## ✨ Core Features

### 1. The Velvet Rope (Authentication)
* **Exclusive Access:** Strict domain restriction using Google Sign-In via Firebase Auth. Only users with valid `@srmap.edu.in` email addresses can access the platform.
* **Auto-Profiles:** Seamlessly generates user profiles by pulling Display Names and Photo URLs directly from Google.

### 2. The Live Radar (Dashboard)
* **Dynamic Feed:** A clean, card-based interface displaying active beacons across the campus.
* **Targeted Filtering:** Sort beacons by categories such as Study 📚, Food 🍔, Chill 🎮, and Sports 🏏.

### 3. Beacon Creation
* **Rapid Setup:** Users can broadcast an activity, select a location from campus dropdowns (e.g., Library, Adarsh Mess), and set an auto-expiry timer (1-2 hours).
* **Smart Party Sizing:** The system precisely calculates and displays the exact number of *additional* spots needed, automatically excluding the host from the remaining participant count.

### 4. The Lobby & GenAI Icebreakers
* **Instant Connection:** Clicking "Join" drops the user into a temporary, real-time group chat specific to that Beacon.
* **AI-Powered Icebreakers:** Integrated with the **Google Gemini Flash API**, the system automatically posts a context-aware, funny one-liner into the chat based on the chosen activity to eliminate initial awkwardness.

---

## 🛠️ Technical Stack

* **Frontend:** React + Vite (Optimized for speed)
* **Styling:** Tailwind CSS (Clean, minimalist, and responsive UI) + Lucide React (Icons)
* **State Management:** React Context API
* **Backend & Database:** Firebase (Firestore + Authentication)
* **AI Integration:** Google Gemini Flash API (via `@google/generative-ai` SDK)

---

## 🚀 Local Development Setup

To run this project locally, clone the repository and follow these steps:

### 1. Install Dependencies
```bash
npm install
