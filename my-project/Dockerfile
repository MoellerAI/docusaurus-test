# Use a lightweight Node.js image
FROM node:18-alpine

# Set working directory
WORKDIR /app

# Copy package.json and package-lock.json for better caching
COPY package.json package-lock.json ./

RUN npm install

# Copy the rest of the application files
COPY . .

# Expose the Docusaurus development server port
EXPOSE 3000

# Start the Docusaurus development server
CMD ["npm", "run", "start", "--", "--host", "0.0.0.0"]