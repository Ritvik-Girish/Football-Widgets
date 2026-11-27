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
