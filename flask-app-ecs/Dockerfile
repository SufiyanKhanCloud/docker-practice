# Base Image
# stage 1 has base image 994mb ~ 1.04 Gb
FROM python:3.7 AS builder 

# Working Directory
WORKDIR /app

# Copy requirements.txt from host to containers working directory
COPY requirements.txt .

# Install the Dependencies
RUN pip install -r requirements.txt

# -------
# stage 2 base image 125mb ~ 142mb
FROM python:3.7-slim

WORKDIR /app

COPY --from=builder /usr/local/lib/python3.7/site-packages/ /usr/local/lib/python3.7/site-packages/

COPY . .

# Run the Code
ENTRYPOINT ["python","run.py"]
