
# 🎨 Virtual Museum

A lightweight Flask web application that lets you **curate, browse, and manage artwork online**.  
It ships with an in-memory MongoDB mock (`mongomock`) so you can run, test, and demo the app with **zero external dependencies**.

---

## Table of Contents

1. [Demo](#-demo)
2. [Features](#-features)
3. [Tech Stack](#-tech-stack)
4. [Quick Start](#-quick-start)
5. [Project Structure](#-project-structure)
6. [Usage Guide](#-usage-guide)
7. [Configuration](#-configuration)
8. [Results & Screenshots](#-results--screenshots)
9. [Roadmap](#-roadmap)
10. [Contributing](#-contributing)
11. [License](#-license)
12. [Author](#-author)

---

## 📺 Demo

> _Coming soon_ – record a short GIF or link to a live deployment here!

---

## ✨ Features

| Category           | Details                                                                    |
|--------------------|-----------------------------------------------------------------------------|
| CRUD Operations    | Add, view, edit, and delete artworks with basic form validation.            |
| Search             | Full-text search across **title, artist, and description** fields.          |
| Bootstrap UI       | Clean, responsive interface powered by Bootstrap 5 (via CDN).               |
| Seed Data          | Auto-populates a few famous artworks on first run for instant testing.      |
| Zero DB Setup      | Uses **`mongomock`** – no separate MongoDB server required.                 |
| WTForms + Flask-WTF| CSRF-protected forms, client-side & server-side validation.                 |
| Modular Code       | Single `app.py`, clear route breakdown, easy to extend or plug into MongoDB.|

---

## ⚙️ Tech Stack

- **Python 3.10 +**
- **Flask 2.3**
- **Flask-WTF 1.1 / WTForms 3**
- **mongomock 4** (in-memory MongoDB replacement)
- **Bootstrap 5** (CDN)

---

## 🚀 Quick Start

```bash
# 1) Clone the repo
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>/etb

# 2) (Recommended) Create & activate a virtual environment
python -m venv .venv
source .venv/bin/activate            # Windows: .venv\Scripts\activate

# 3) Install dependencies
pip install -r requirements.txt

# 4) Launch the server
python app.py                        # or: flask run

# 5) Visit the app
# Open http://127.0.0.1:5000 in your browser
```

_By default the app seeds several famous paintings so you can explore immediately._

---

## 📁 Project Structure

```
.
└── etb
    ├── app.py                # Core Flask application
    ├── requirements.txt      # Pinned Python dependencies
    └── templates/            # Jinja2 templates
        ├── base.html
        ├── index.html
        ├── artworks.html
        ├── artwork_detail.html
        ├── new_artwork.html
        └── edit_artwork.html
```

---

## 🛠️ Usage Guide

| URL / Route                 | Purpose                                 | Template                  |
|-----------------------------|-----------------------------------------|---------------------------|
| `/`                         | Landing page                            | `index.html`              |
| `/artworks`                 | List all artworks                       | `artworks.html`           |
| `/artworks/new`             | Create a new artwork                    | `new_artwork.html`        |
| `/artworks/<id>`            | Show artwork details                    | `artwork_detail.html`     |
| `/artworks/<id>/edit`       | Edit an existing artwork                | `edit_artwork.html`       |
| `/artworks/<id>/delete`     | Delete artwork (POST)                   | –                         |
| `/search?query=<keyword>`   | Search artworks (title/artist/desc)     | `artworks.html` (filtered)|

---

## 🔧 Configuration

| Variable        | Default            | Description                                    |
|-----------------|--------------------|------------------------------------------------|
| `FLASK_ENV`     | `development`      | Set to `production` for prod deployments.      |
| `SECRET_KEY`    | `your_secret_key`  | Replace with a strong, random value in prod.   |
| `MONGO_URI`     | _not set_          | Configure this + remove `mongomock` to use a real MongoDB server. |

---

## 🖼️ Results & Screenshots

> Drop a few screenshots or performance metrics if you have them (e.g., Lighthouse scores).

---

## 🗺️ Roadmap

- [ ] **Real MongoDB support** – swap `mongomock` for `PyMongo`, parameterize connection string.  
- [ ] **Image uploads** – store user-uploaded artwork images (local or cloud storage).  
- [ ] **User authentication** – multi-user galleries, favorites, comments.  
- [ ] **REST / GraphQL API** – decouple front-end and back-end.  
- [ ] **Dockerfile** – containerize for easy CI/CD & deployment.

---

## 🤝 Contributing

1. Fork the repository.  
2. Create a feature branch: `git checkout -b feat/awesome-feature`.  
3. Commit your changes: `git commit -m "Add awesome feature"`.  
4. Push to the branch: `git push origin feat/awesome-feature`.  
5. Open a Pull Request – we’ll review it together!

### Code Style

- Follow **PEP 8** where practical.  
- Use **black** & **isort** for formatting (`pip install black isort`).  
- Write small, focused commits with clear messages.

---

## 📄 License

Distributed under the **MIT License**.  
See `LICENSE` for more information.

---

## 🙋‍♀️ Author

**Helan Xavier** – _Data Science enthusiast & budding full-stack developer_  
📫 Reach me on **LinkedIn** / **Twitter** / **Email** (update with links).

> If you find this project useful, please ⭐ star the repo and share it with fellow art lovers!
