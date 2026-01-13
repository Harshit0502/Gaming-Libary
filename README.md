# Gaming Library (Vue.js + Flask Full-Stack SPA)

A simple full-stack “Game Library” app built with **Vue 2** (SPA) on the frontend and a **Flask REST API** on the backend.  
You can **view, add, update, and delete** games from a small in-memory list.

---

## Tech Stack

- **Frontend:** Vue 2, Vue Router, Axios, Bootstrap / Bootswatch
- **Backend:** Flask, Flask-CORS

---

## Project Structure

```

Gaming-Libary-main/
backend/
main.py
requirements.txt
Pipfile
frontend/
frontend/          # Vue CLI app lives here
package.json
src/
components/
Games.vue
Shark.vue
router/
index.js

````

---

## Features

- **Games CRUD**
  - List games
  - Add a new game
  - Update an existing game
  - Delete a game
- **Test route:** `/shark` (frontend) calling `/shark` (backend)

---

## API Endpoints (Flask)

Base URL: `http://localhost:5000`

- `GET /` → `"Hello, world!"`
- `GET /shark` → `"Shark🦈!"`
- `GET /games` → returns all games
- `POST /games` → adds a game  
  **Body (JSON):**
  ```json
  { "title": "GTA V", "genre": "action", "played": true }


* `PUT /games/<game_id>` → updates a game
  **Body (JSON):**

  ```json
  { "title": "GTA V", "genre": "action", "played": false }
  ```
* `DELETE /games/<game_id>` → removes a game

✅ CORS is enabled for all origins in this project.

---

## Run Locally

### 1) Start the Backend (Flask)

```bash
cd backend

# (recommended) create a venv
python -m venv .venv

# activate it
# Windows (PowerShell): .\.venv\Scripts\Activate.ps1
# macOS/Linux:
source .venv/bin/activate

pip install -r requirements.txt
python main.py
```

Backend runs at: `http://localhost:5000`

---

### 2) Start the Frontend (Vue)

```bash
cd frontend/frontend
npm install
npm run serve
```

Frontend runs at: `http://localhost:8080`

Try:

* `http://localhost:8080/games`
* `http://localhost:8080/shark`

---

## Troubleshooting

* If Vue shows **“Cannot find module 'bootstrap-vue'”**, install it:

  ```bash
  npm i bootstrap-vue
  ```
* If you see literal `...` inside Vue files (like `Games.vue` / `Shark.vue`) that causes build errors, remove those `...` lines—they’re not valid JS/Vue code.

---

```
```
