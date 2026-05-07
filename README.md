# CoNexus - Premium Publishing Platform

CoNexus is a fully interactive, state-of-the-art blog and article publishing platform. Built with a robust Flask backend and an ultra-modern, glassmorphic frontend utilizing Tailwind CSS, CoNexus delivers a premium, app-like experience for both readers and creators.

## ✨ Platform Highlights

### 🎨 Next-Generation UI/UX
- **Glassmorphic Design System**: Premium aesthetic featuring frosted glass effects, deep space mesh gradients, and floating components.
- **Fluid Dark/Light Mode**: Seamless, system-wide theme toggling with smooth, instantaneous transitions.
- **App-Like Shell**: Fixed sidebar navigation, sticky headers, and responsive layouts that look exceptional on mobile and desktop alike.

### ✍️ Creator Tools
- **Distraction-Free Editor**: A clean, focused writing interface for authors to craft their stories without visual clutter.
- **Smart Publishing Controls**: Side-by-side editing and publishing options including featured tags, category selection, and instant image previews.
- **Dynamic Character Counters & Auto-resizing Textareas**: Enhances the ergonomic feel of content creation.

### 🛡️ Administration & Moderation
- **Command Center Dashboard**: Visual data cards capturing total posts, views, and comments.
- **Flat UI Data Tables**: Refined, searchable, and filterable tables for managing a growing catalog of content.
- **Interactive Comment Moderation**: Direct inline actions to approve or delete community interactions.

### 🧩 Core Features
- **Authentication**: Split-panel login and registration screens.
- **Engaging Error States**: Custom cosmic (`404`) and glitch (`500`) animated error pages ensuring even dead-ends feel premium.
- **Contextual Interactions**: Micro-animations on hover states, reading progress bars, and floating action buttons.

---

## 🛠️ Technology Stack

- **Backend Framework**: Python / [Flask](https://flask.palletsprojects.com/)
- **Frontend Styling**: [Tailwind CSS](https://tailwindcss.com/) (via CDN) & Custom CSS (`app.css`)
- **Database**: SQLite (SQLAlchemy ORM)
- **Authentication**: Flask-Login
- **Icons**: Font Awesome

---

## 📁 Project Architecture

```text
CoNexus/
├── app.py                 # Core Flask application & routing
├── requirements.txt       # Python dependencies
├── README.md              # Project documentation
├── templates/             # Jinja2 HTML templates
│   ├── base.html          # App shell (Sidebar, Navbar, Theme toggles)
│   ├── home.html          # Discover page (Hero, Latest Feed)
│   ├── blog.html          # Explore page (Bento grid, Search, Filters)
│   ├── post.html          # Reading interface (Content, Comments)
│   ├── auth/              # login.html & register.html
│   ├── user/              # Dashboard, create_post.html, edit_post.html
│   ├── admin/             # Control panel, moderation, post oversight
│   └── errors/            # 404.html (Lost in Space) & 500.html (Glitch)
├── static/                
│   ├── css/app.css        # Premium design tokens and animations
│   └── uploads/           # User-uploaded featured images
└── blog.db                # SQLite database (Auto-generated)
```

---

## 🚀 Quick Start Local Setup

### 1. Prerequisites
- Python 3.8+
- pip

### 2. Installation Setup

Clone the repository and initialize a virtual environment:

```bash
git clone <repository-url>
cd conexus

# Create virtual environment
python -m venv venv

# Activate (Windows)
venv\Scripts\activate
# Activate (macOS/Linux)
source venv/bin/activate
```

Install the required Python dependencies:

```bash
pip install -r requirements.txt
```

### 3. Launching the App

Start the Flask development server:

```bash
python app.py
```

- Navigate your browser to: `http://localhost:5000`
- **Default Admin Credentials:** Check deployment configuration or register a new user and escalate privileges via database.

---

## 📊 Database Schema Summary

The platform uses SQLAlchemy with the following core entities:

- **User**: Handles authentication (`username`, `email`, `password_hash`, `is_admin`).
- **Post**: Stores blog content (`title`, `slug`, `content`, `featured_image`, publication statuses, view counts).
- **Category**: Classifies posts contextually.
- **Comment**: Community interactions bound to specific Posts and Users (`is_approved` flag included for moderation).

---

## 🎨 Customizing the Design System

The core aesthetic logic resides in `static/css/app.css`. 
* Ensure changes adhere to standard CSS variables if extending the primary/secondary color maps. 
* Tailwind classes are composed directly within the Jinja templates.
* **Micro-animations** (like `.fade-in`, `.stagger`, `@keyframes shake`) are globally available for injection.

---

## 📝 License

This project is open-source and available under the terms of the MIT License.

---
*Built with ❤️ for storytellers.*
