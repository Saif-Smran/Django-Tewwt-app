# Django Tweet App

A lightweight Twitter-style microblog built with Django 5. Users can register, log in, and post short tweets (up to 280 characters) with an optional photo. Tweets are shown newest-first, and authors can edit or delete their own posts.

## Features
- User auth: register, login, logout (Django auth views)
- Create, edit, and delete tweets
- Optional image upload per tweet (uses Pillow)
- Bootstrap 5 dark theme layout
- Media served locally via `MEDIA_URL`/`MEDIA_ROOT`

## Quick Start
```pwsh
# From the project root
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt

# Apply migrations and run
cd caiheadq
python manage.py migrate
python manage.py runserver
```

Visit `http://127.0.0.1:8000/tweet/` for the feed.
- Register: `http://127.0.0.1:8000/tweet/register/`
- Login/Logout: `http://127.0.0.1:8000/accounts/login/` and `/accounts/logout/`
- Create new tweet: `http://127.0.0.1:8000/tweet/new/`

Uploads are stored under `media/tweets/photos/` (served in development).

## Tech Stack
- Django `5.2.8`
- Pillow `12.0.0` (image handling)
- SQLite (default)

---
Project module: `tweet`
Key entry points: `caiheadq/urls.py` and `tweet/urls.py`
