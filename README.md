# k8s-core-concepts

This is a simple FastAPI application demonstrating basic Kubernetes core concepts. It serves a simple JSON response `{"message": "Hello World"}` on the root endpoint.

## Project Structure

- `app/main.py`: The FastAPI application code.
- `requirements.txt`: Python dependencies (`fastapi`, `uvicorn`).
- `Dockerfile`: Instructions to build the Docker image for the application.

## Running Locally

To run the application locally without Docker, follow these steps:

1. Create a virtual environment (optional but recommended):

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Run the application:

   ```bash
   cd app
   uvicorn main:app --reload
   ```

   The app will be available at `http://127.0.0.1:8000`.

## Docker

You can also build and run the application using Docker:

1. Build the Docker image:

   ```bash
   docker build -t k8s-core-concepts-app .
   ```

2. Run the Docker container:

   ```bash
   docker run -p 80:80 k8s-core-concepts-app
   ```

   The app will be available at `http://localhost:80` (or the IP of your Docker host).
