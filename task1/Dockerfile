FROM ubuntu:latest

# Avoid user interaction
ENV DEBIAN_FRONTEND=noninteractive

# Update and install python & pip
RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y python3 python3-pip

# Fix "externally managed environment" issue
RUN rm -f /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask via pip3 (NOT apt)
RUN pip3 install flask

# Set working directory
WORKDIR /app

# Copy Python API file
COPY ./api.py /app/api.py

# Run the Flask app on container start
CMD ["python3", "/app/api.py"]
