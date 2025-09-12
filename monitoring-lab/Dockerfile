FROM python:3.10-slim

WORKDIR /app

# Copier les fichiers de requirements
COPY requirements.txt .

# Installer les dépendances
RUN pip install --no-cache-dir -r requirements.txt

# Copier le code de l'application
COPY main.py .

# Exposer le port
EXPOSE 5000

# Commande par défaut
CMD ["gunicorn", "--bind", "0.0.0.0:5000", "main:app"]