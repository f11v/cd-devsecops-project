# 1. Cambia esta línea por una imagen más segura
FROM python:3.9-slim-bookworm

WORKDIR /app

# 2. Usa requirements.txt para instalar dependencias de forma consistente
COPY requirements.txt .
RUN pip install --no-cache-dir --upgrade pip setuptools && pip install --no-cache-dir -r requirements.txt

# Copia el resto del código de la aplicación
COPY . .

EXPOSE 5000

# 3. Corrige el nombre del archivo a ejecutar
CMD ["python", "MAIN.PY"]