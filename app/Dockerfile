# Probamos con la combinación más moderna: Python 3.12 sobre Debian Bookworm
FROM python:3.12-slim-bookworm

# El resto de tu Dockerfile sigue igual...
RUN apt-get update && apt-get upgrade -y && rm -rf /var/lib/apt/lists/*
WORKDIR /app
COPY requirements.txt .
RUN pip install --no-cache-dir --upgrade pip setuptools
RUN pip install --no-cache-dir -r requirements.txt
COPY . .
CMD ["python", "app.py"]