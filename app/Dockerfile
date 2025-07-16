# 1. Usar la imagen base segura y ligera de Alpine
FROM python:3.9-alpine

WORKDIR /app

COPY requirements.txt .

# 2. Actualizar pip y setuptools ANTES de instalar las dependencias
#    Esta es la línea clave que faltaba para arreglar todo.
RUN pip install --no-cache-dir --upgrade pip setuptools && pip install --no-cache-dir -r requirements.txt

COPY . .

EXPOSE 5000
CMD ["python", "MAIN.PY"]