# Use the official Python image from the Docker Hub
FROM python:3.10-slim

# Install packages
RUN apt-get update && apt-get install -y \
    pciutils \
    curl \
    nano \
    && rm -rf /var/lib/apt/lists/*

# Set the working directory in the container
WORKDIR /app

# Copy the requirements file into the container
COPY requirements.txt .

# Update pip
RUN pip install --upgrade pip

# Install the necessary packages
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application code into the container
COPY . .

# Make port 53 available to the world outside this container
EXPOSE 53/udp

# Define environment variable
ENV NAME DNS_Server

# Run app.py when the container launches
CMD ["python", "/app/dns_server.py"]
