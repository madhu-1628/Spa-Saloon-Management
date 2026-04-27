# LuxeSpa Saloon & Spa Management

<div align="center">
  <h3>✂️ Premium Unisex Spa & Salon – Full Stack Application</h3>
  <p>Frontend: HTML · CSS · JavaScript · Three.js &nbsp;|&nbsp; Backend: Java Spring Boot · H2</p>
</div>

---

## 🚀 Quick Start

### Option 1 – One-Click Launch (Windows)
Double-click **`START_APP.bat`** — it will start the backend and open the frontend automatically.

### Option 2 – Manual

**Backend (requires Java 17+ and Maven):**
```bash
cd backend
mvn spring-boot:run
```
Backend runs at: **http://localhost:8080**

**Frontend:**
Simply open `frontend/index.html` in any modern browser.  
> The app works fully even without the backend running (all pages show static data gracefully).

---

## 📁 Project Structure

```
SPAandSALOON/
├── START_APP.bat               ← One-click launcher
├── README.md
│
├── frontend/
│   ├── index.html              ← Landing page + 3D Three.js scene
│   ├── login.html              ← Login / Registration
│   ├── recommendation.html     ← 5-step AI recommendation quiz
│   ├── booking.html            ← 4-step booking wizard + Leaflet map
│   ├── css/
│   │   └── style.css           ← Full design system (glassmorphism, parallax, animations)
│   ├── js/
│   │   └── main.js             ← Three.js 3D scene, parallax, scroll reveals, toast, tilt
│   └── assets/
│       └── hero-bg.jpg         ← Luxury spa background image
│
└── backend/
    ├── pom.xml                 ← Maven (Spring Boot 3, JPA, H2)
    └── src/main/java/com/spa/saloon/
        ├── SaloonApplication.java          ← Entry point + CORS config
        ├── model/Booking.java              ← JPA entity
        ├── repository/BookingRepository.java
        └── controller/
            ├── BookingController.java      ← POST/GET /api/bookings
            ├── ServiceController.java      ← GET /api/services, /offers, /recommendations
            └── AuthController.java         ← POST /api/auth/login
```

---

## 🌟 Features

| Page | Features |
|------|----------|
| **Home** | 3D interactive Three.js salon scene (scissors, chair, dryer, mirror), golden particle rain, parallax hero, service cards with 3D tilt, offers, animated counters, testimonials, marquee ribbon |
| **Login** | Split-screen auth view, animated login/register tab switch, backend API call with demo fallback, social login buttons |
| **Recommendations** | 5-step smart quiz, per-answer AI matching score, dynamic result cards with animated progress bars, loads live services from backend |
| **Booking** | 4-step wizard (service → date/time → info → confirm), interactive time slot grid, Leaflet.js dark map (Mumbai), discount auto-apply, confetti success animation, backend POST |

### 🎨 Design System
- **Theme:** Dark luxury with gold accents (`#c9a96e`)
- **Typography:** Playfair Display (headings) + Inter (body)
- **Effects:** Glassmorphism cards, cursor glow, scroll-reveal, micro-animations, marquee, parallax

---

## 🔌 REST API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| `POST` | `/api/auth/login` | Login with email/password |
| `GET` | `/api/services` | List all services |
| `GET` | `/api/services/offers` | Get current discount offers |
| `GET` | `/api/services/recommendations` | Get top recommendations |
| `POST` | `/api/bookings` | Create a new booking |
| `GET` | `/api/bookings` | List all bookings |
| `GET` | `/h2-console` | View in-memory database (dev only) |

---

## 🛠️ Tech Stack

**Frontend**
- Vanilla HTML5, CSS3, JavaScript (ES6+)
- [Three.js r128](https://threejs.org/) – 3D WebGL rendering
- [Leaflet.js 1.9](https://leafletjs.com/) – Interactive map
- Google Fonts (Playfair Display, Inter)

**Backend**
- Java 17
- Spring Boot 3.2
- Spring Data JPA
- H2 In-Memory Database
- Maven

---

## 📸 Pages Overview

- `/frontend/index.html` – Landing page with animated 3D salon scene
- `/frontend/login.html` – Auth portal
- `/frontend/recommendation.html` – Smart quiz + personalised results
- `/frontend/booking.html` – Full appointment booking with map

---

*Built with ❤️ for LuxeSpa Saloon — Mumbai's Premier Unisex Spa & Salon*
