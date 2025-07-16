# Usa una imagen base específica y actualizada
FROM python:3.10-slim-bookworm

# Actualiza los paquetes del SO a sus últimas versiones
RUN apt-get update && apt-get upgrade -y && rm -rf /var/lib/apt/lists/*

WORKDIR /app
COPY ./app/requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
COPY ./app .
CMD ["python", "app.py"]