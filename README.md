# Flask Blog Application

This repository contains a simple blog platform built with Flask as part of the "100 Days of Code" challenge. It supports user registration/login, creating and editing posts, and commenting.

## Features

- User authentication (register, login, logout) using Flask-Login
- Password hashing with Werkzeug
- Create, edit, and delete blog posts (admin only)
- Commenting on posts with CKEditor rich text
- Gravatar integration for user avatars
- Bootstrap5 for responsive styling
- SQLite database via SQLAlchemy ORM

## Getting Started

### Prerequisites

- Python 3.10+ (or compatible) installed on your system
- `pip` for package management

### Installation

1. Clone the repository:
   ```bash
   git clone <repo-url>
   cd "Blog 4"
   ```

2. Create and activate a virtual environment:
   ```bash
   python -m venv venv
   # Windows
   venv\Scripts\activate
   # macOS/Linux
   source venv/bin/activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Copy the example environment file and set a secret key:
   ```bash
   copy .env.example .env   # Windows
   cp .env.example .env     # macOS/Linux
   ```
   Edit `.env` and provide a secure value for `SECRET_KEY`.

5. Run the app:
   ```bash
   python main.py
   ```
   The application will be available at `http://localhost:5002`.

## Usage

- Register a new user or login with an existing account.
- Post comments only when logged in.
- Only the first registered user (ID 1) can create, edit or delete posts.

## Database

The SQLite database file (`posts.db`) is automatically created in the project root the first time the app runs.

## Environment Variables

- `SECRET_KEY` — used by Flask for session and CSRF protection. Keep this value secret.

## Notes

- `.env` is ignored by git. Make sure it is not committed with real secrets.
- Delete or rotate the secret key if it becomes exposed.

---
