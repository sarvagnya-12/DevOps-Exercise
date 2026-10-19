FROM python:3.9-slim
RUN apt-get update && apt-get install -y iputils-ping && rm -rf /var/lib/apt/lists/*
WORKDIR /app
COPY requirements.txt .
COPY app.py .
RUN pip install --no-cache-dir -r requirements.txt "werkzeug<2.1"
EXPOSE 5001
CMD ["python", "app.py"]