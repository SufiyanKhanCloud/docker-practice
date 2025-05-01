# Base Image
FROM python:3.7 

# Working Directory
WORKDIR /app

# Copy from host/source to containers working directory
COPY . .

# Install the Dependencies
RUN pip install -r requirements.txt

# Run the Code
ENTRYPOINT ["python","run.py"]
