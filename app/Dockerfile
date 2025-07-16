# Usa una imagen base específica y actualizada
FROM python:3.10-slim-bookworm

# Actualiza los paquetes del SO a sus últimas versiones
# This command helps fix OS vulnerabilities like the one in zlib1g
RUN apt-get update && apt-get upgrade -y && rm -rf /var/lib/apt/lists/*

WORKDIR /app

COPY requirements.txt .

# Upgrade pip and setuptools to fix package vulnerabilities FIRST
RUN pip install --no-cache-dir --upgrade pip setuptools

# Now install the rest of the dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copia todo el contenido del contexto (el resto de los archivos de ./app)
COPY . .

CMD ["python", "app.py"]