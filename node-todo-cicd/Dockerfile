# Node Base Image
FROM node:12.2.0-alpine

# Working Directory
WORKDIR /node

# Copy the code from host/source to containers working directory
COPY . .

# Install the Dependencies
RUN npm install
RUN npm run test
EXPOSE 8000

# Run the Code
CMD ["node","app.js"]
