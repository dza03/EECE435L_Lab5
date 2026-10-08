# Lab 5 – Flask User API + Postman

## Files
- `database.py` – SQLite database functions (create table, add, get, update, delete users)
- `app.py` – Flask REST API that exposes the database functions
- `database.db` – the SQLite database
- `Flask user app.postman_collection.json` – Postman collection (all 5 requests + saved examples)
- `screenshots/` – screenshots of each API request and its result

## How to run
```
python -m venv venv
venv\Scripts\activate        (Mac: source venv/bin/activate)
pip install -r requirements.txt
python app.py
```
The server runs on http://localhost:5000

## How to test with Postman
1. Import `Flask user app.postman_collection.json` into Postman (Import → select file).
2. Create an environment with a variable `base_url` = `http://localhost:5000` and select it.
3. Run the requests in this order: Add User → Get All Users → Get User By ID → Update User → Delete User.

## Endpoints
| Method | URL | What it does |
|---|---|---|
| GET | /api/users | Get all users |
| GET | /api/users/<user_id> | Get one user |
| POST | /api/users/add | Add a user |
| PUT | /api/users/update | Update a user |
| DELETE | /api/users/delete/<user_id> | Delete a user |