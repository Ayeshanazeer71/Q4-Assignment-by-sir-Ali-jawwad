 # DACA Chatbot API 🚀

This project is a modern FastAPI application demonstrating the use of **Pydantic** for robust data validation and structured agent communication. It simulates a chatbot interface where user messages (with metadata) are handled and responded to by the API.

---

## 🔧 Technologies Used

- **FastAPI** – For creating high-performance web APIs with automatic documentation.
- **Pydantic** – For data validation, serialization, and nested model management.
- **Uvicorn** – For running the FastAPI app with automatic reload.
- **Python 3.11+**

---

## 📦 Project Setup

### Step 1: Initialize Environment

Create a new virtual environment and install the required packages:

```bash
uv init fastdca_p1
cd fastdca_p1
uv venv
source .venv/bin/activate  # Use `.venv\Scripts\activate` on Windows
uv add "fastapi[standard]"
📘 Key Concepts
🧩 What is Pydantic?
Pydantic ensures reliable and type-safe handling of data by validating against Python type hints. It plays a central role in FastAPI to manage request and response data.

Pydantic Features:
Strict type-checking and conversion (e.g., "123" → 123)

Clear validation error messages

Support for complex/nested schemas

JSON serialization/deserialization

Custom validation logic using decorators

📂 Project Structure
bash
Copy
Edit
fastdca_p1/
│
├── main.py                 # Main FastAPI application
├── pydantic_example_1.py  # Basic model validation example
├── pydantic_example_2.py  # Nested Pydantic models
└── pydantic_example_3.py  # Custom validators with error handling
⚙️ Running the App
To start the development server:

bash
Copy
Edit
uvicorn main:app --reload
Then open your browser and visit:

bash
Copy
Edit
http://localhost:8000/docs
This will show FastAPI's automatic Swagger UI documentation.

🧠 API Endpoints
/ – Root
Method: GET

Description: Welcome message for the API.

/users/{user_id} – Fetch User Info
Method: GET

Query Parameters: role (optional)

Returns: User ID and role info.

/chat/ – Chat Interface
Method: POST

Body: JSON containing user ID, message text, and metadata

Returns: Structured reply with a generated timestamp and session ID.

Example Request Body:

json
Copy
Edit
{
  "user_id": "ayesha123",
  "text": "Hello chatbot!",
  "metadata": {
    "timestamp": "2025-05-09T10:00:00Z",
    "session_id": "abc123-session"
  },
  "tags": ["greeting", "user"]
}
📈 Why Use Pydantic in This Project?
Ensures data accuracy in AI workflows

Helps avoid runtime bugs with static type enforcement

Automatically provides readable validation errors

Makes API contracts more transparent with JSON schemas

📬 Contact
For questions or feedback, feel free to reach out to the project maintainer.

🚀 Ready to explore?
Run the app and go to /docs or /redoc to interact with the API!


