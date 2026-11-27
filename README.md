<div align="center">

# ⚽ Universal Football Widget

**A sleek, macOS-inspired glassmorphic desktop widget for tracking live football standings, stats, and upcoming fixtures across Europe's top five leagues.**

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Zero Dependencies](https://img.shields.io/badge/Dependencies-Zero-success?style=for-the-badge)

</div>

---

## 📖 Overview

**Universal Football Widget** is a lightweight, zero-dependency desktop component built with vanilla HTML, CSS, and JavaScript. Designed to sit cleanly over desktop wallpapers via transparent web-view containers (such as **WidgetWall** on Windows or **Übersicht** on macOS), it dynamically adapts its accent palette to match your selected club's colors while pulling live standings and fixture data from ESPN's public endpoints.

---

## ✨ Key Features

- **Frosted Glassmorphism UI:** Translucent dark backdrop (`backdrop-filter: blur(32px)`) with subtle specular borders and dynamic radial glow accents tailored to your club's primary kit color (with automatic contrast protection for white kits).
- **Top 5 European Leagues:** Built-in support for the **Premier League**, **La Liga**, **Serie A**, **Bundesliga**, and **Ligue 1** with custom league pill gradients.
- **Live Table & Club Metrics:** Displays current league rank, total points, matches played (`PLD`), wins (`WIN`), draws (`DRW`), losses (`LST`), and goal difference (`GD`).
- **Upcoming Fixtures & Kickoff Times:** Tracks the next three scheduled matches (including home/away indicators and opponent crests) formatted cleanly into local time (`IST`).
- **In-Widget Club Switcher:** Click the gear icon (`⚙`) to switch leagues and clubs on the fly without touching any code.
- **Offline Resilience & Persistence:** Caches the latest fetched data and user preferences in `localStorage` so the widget stays populated even during brief network drops.

---

## 🚀 Installation & Setup

### 1. Download the Widget
Clone the repository or download the source ZIP directly from GitHub:

```bash
git clone [https://github.com/Ritvik-Girish/universal-football-widget.git](https://github.com/Ritvik-Girish/universal-football-widget.git)
```

### 2. Run as a Desktop Widget

#### **Windows (WidgetWall / Rainmeter WebView)**
1. Open **WidgetWall** (or your preferred HTML desktop widget engine) and create a new **Web / HTML Widget**.
2. Point the source path to your downloaded `index.html` file.
3. Enable **Transparent Background** in the widget's window settings (`background: transparent !important;` is already configured in the stylesheet).
4. Set the container dimensions to **`360px` × `285px`** for optimal card proportions.

#### **macOS (Übersicht)**
1. Move the widget folder into your Übersicht widgets directory (`~/Library/Application Support/Übersicht/widgets/`).
2. Point your widget wrapper to `index.html` and position it on your desktop.

> **💡 Local Browser Preview:** If opening `index.html` directly in Chrome or Safari (`file://`), strict browser CORS rules may block external API requests. Serve the folder locally instead:
> ```bash
> npx serve .
> # or
> python3 -m http.server 8080
> ```

---

## ⚙️ Configuration & URL Parameters

You can configure your club directly inside the widget's **Settings Drawer (`⚙`)**, or override the default team at launch by appending query parameters to the widget URL:

```text
index.html?league=esp.1&team=86
```

### Supported League Codes

| League | Country | Query Code (`league=`) |
| :--- | :--- | :--- |
| **Premier League** | England | `eng.1` |
| **La Liga** | Spain | `esp.1` |
| **Serie A** | Italy | `ita.1` |
| **Bundesliga** | Germany | `ger.1` |
| **Ligue 1** | France | `fra.1` |

### Popular Team IDs (`team=`)

| Club | League | ESPN Team ID |
| :--- | :--- | :--- |
| **Manchester United** | `eng.1` | `360` |
| **Liverpool** | `eng.1` | `364` |
| **Arsenal** | `eng.1` | `359` |
| **Real Madrid** | `esp.1` | `86` |
| **FC Barcelona** | `esp.1` | `83` |
| **Bayern Munich** | `ger.1` | `132` |
| **Juventus** | `ita.1` | `111` |
| **Paris Saint-Germain** | `fra.1` | `160` |

---

## 🏗️ Architecture & Tech Stack

- **HTML5 & CSS3:** Semantic layout powered by CSS Custom Properties (`--accent`, `--accent-rgb`, `--accent-fg`), Flexbox, and YIQ brightness calculation for automatic text contrast.
- **Vanilla JavaScript (ES6+):** Non-blocking `Promise.all` data fetching with automatic CORS proxy fallbacks, timeout guards, and `localStorage` state persistence.
- **ESPN Sports Endpoints:** Live JSON feeds for league standings, team metadata, club crests, and match schedules.

---

## 📝 Credits & Acknowledgments

- **Live Match & Standings Data:** Powered by public sports data endpoints and club crest assets from [ESPN FC](https://www.espn.com/).
- **Design & Development:** Created and maintained by **[Ritvik Girish](https://github.com/Ritvik-Girish)**.

---

<div align="center">
  <sub>Built with clean code and football obsession. ⭐ Star this repo if you use it on your setup!</sub>
</div>
