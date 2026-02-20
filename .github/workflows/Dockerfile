# 1. Base image
FROM node:18-alpine

# 2. Set working directory inside container
WORKDIR /app

# 3. Copy package files first (better caching)
COPY package*.json ./

# 4. Install dependencies
RUN npm install --production

# 5. Copy the rest of the project files
COPY . .

# 6. Build step (if your project has one)
RUN npm run build

# 7. Expose port (adjust if your app uses a different one)
EXPOSE 3000

# 8. Default command to start the app
CMD ["npm", "start"]
