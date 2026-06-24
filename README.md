# JoinIn 

> **The "Just-in-Time" Connection Layer for the SRM AP Campus.**
> *Built for the Code For Connection (Web/Mobile Development) Hackathon.*

---

## 🌐 Live Demo

🚀 https://joinin-srm.web.app/

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
```
**2. Environment Variables**
Create a .env file in the root directory and add your specific API keys. Do not commit this file to version control.
```bash
Code snippet
VITE_FIREBASE_API_KEY=your_firebase_api_key
VITE_FIREBASE_AUTH_DOMAIN=your_firebase_auth_domain
VITE_FIREBASE_PROJECT_ID=your_firebase_project_id
VITE_GEMINI_API_KEY=your_gemini_api_key
```
**3. Start the Development Server**
```Bash
npm run dev
```
## 🗺️ Routing Structure
* **/ - Landing Page & Google Login**

* **/dashboard - Main Feed (The Live Radar)**

* **/create - Create Beacon Modal/Page**

* **/beacon/:id - The Lobby (Real-time Chat Room)**

## 🔮 Future Scope
Geo-fencing validation to ensure users are physically on campus.

Reputation System to encourage reliable attendance.

Calendar Sync for planned study sessions.
