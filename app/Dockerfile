# Usa una imagen base específica y actualizada
FROM python:3.10-slim-bookworm

# Actualiza los paquetes del SO a sus últimas versiones
RUN apt-get update && apt-get upgrade -y && rm -rf /var/lib/apt/lists/*

WORKDIR /app

# Como el contexto es ./app, copia directamente el archivo
COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

# Copia todo el contenido del contexto (el resto de los archivos de ./app)
COPY . .

CMD ["python", "app.py"]