FROM python:3.10-slim

EXPOSE 5000

# Keeps Python from generating .pyc files in the container
ENV PYTHONDONTWRITEBYTECODE=1

# Turns off buffering for easier container logging
ENV PYTHONUNBUFFERED=1

WORKDIR /app
COPY . /app

# Install pip requirements
RUN pip install --upgrade pip
COPY requirements.txt .
RUN pip install -r requirements.txt

# Run the Flask server on localhost
CMD ["python3", "-m", "flask", "run", "--host=0.0.0.0"]