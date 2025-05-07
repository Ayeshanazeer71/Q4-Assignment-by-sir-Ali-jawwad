  # 🚀 FastAPI Hello World App

This is a simple **FastAPI** application that demonstrates how to build a basic API with Python. It includes two routes:  
- One for a welcome message  
- Another for handling dynamic path and query parameters.

---

## 📌 Features

- Built using [FastAPI]
- Serves a simple "Hello World" JSON response
- Handles dynamic route with query parameters
- Runs with `uvicorn` for fast and efficient development

---

## 🛠️ Requirements

Make sure Python is installed (preferably Python 3.10 or newer).

```bash
python --version

pip install uv


📁 Setup Instructions
Create a project folder

bash
Copy
Edit
mkdir fastapi-hello
cd fastapi-hello
Create a virtual environment

bash
Copy
Edit
uv venv
Activate the virtual environment

Windows:

bash
Copy
Edit
.venv\Scripts\activate
Mac/Linux:

bash
Copy
Edit
source .venv/bin/activate
Install FastAPI and Uvicorn

bash
Copy
Edit
uv pip install "fastapi[all]" uvicorn
📄 Code: main.py
python
Copy
Edit
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def read_root():
    return {"Hello": "World"}

@app.get("/items/{item_id}")
def read_item(item_id: int, q: str | None = None):
    return {"item_id": item_id, "q": q}
▶️ How to Run the Server
Make sure you're in the same directory as main.py, then run:

bash
Copy
Edit
uvicorn main:app --reload
--reload: Enables auto-reloading for development.

🌐 API Endpoints
Method	Endpoint	Description
GET	/	Returns {"Hello": "World"}
GET	/items/{item_id}	Returns item and optional query

Example:

bash
Copy
Edit
http://127.0.0.1:8000/items/42?q=test
Response:

json
Copy
Edit
{
  "item_id": 42,
  "q": "test"
}
📚 Useful Commands Summary
Command	Description
uv venv	Create virtual environment
uv pip install	Install dependencies
uvicorn main:app --reload	Run FastAPI server
.venv\Scripts\activate	Activate venv on Windows
source .venv/bin/activate	Activate venv on Mac/Linux

🧠 Author
This project was created by [Ayesha Nazeer].

