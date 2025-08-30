# Dockerfile to serve MLflow model with FastAPI
FROM python:3.13-slim
WORKDIR /app
COPY docker/requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
COPY api/app.py ./api/app.py
CMD ["uvicorn", "api.app:app", "--host", "0.0.0.0", "--port", "8080"]
