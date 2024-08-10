# Use the slimmer base image similar to the first Dockerfile
FROM python:3.9-slim-buster

# Set the working directory
WORKDIR /usr/src/app

# Copy requirements file and install dependencies
COPY requirements.txt /usr/src/app/
RUN pip install --no-cache-dir -r requirements.txt

# Copy application files and templates
COPY app.py /usr/src/app/
COPY templates /usr/src/app/templates/

# Expose port
EXPOSE 5000

# Set environment variable for Flask
ENV FLASK_APP=app.py

# Run the application
CMD ["flask", "run", "--host", "0.0.0.0"]
