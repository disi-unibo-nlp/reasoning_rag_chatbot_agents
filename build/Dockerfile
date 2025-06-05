# Use the official lightweight Python image
FROM python:3.11-slim

LABEL maintainer="disi-unibo-nlp-LorMolf"

# Set the working directory inside the container
WORKDIR /app

RUN apt-get update && apt-get install -y make

# Copy the requirements file into the container
COPY build/requirements.txt .

# Install pip and setuptools
RUN pip install --upgrade pip setuptools

# Install the dependencies
RUN pip install --no-cache-dir -r requirements.txt

EXPOSE 8080

# Back to default frontend
ENV DEBIAN_FRONTEND=dialog
