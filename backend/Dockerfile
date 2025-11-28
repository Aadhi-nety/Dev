FROM node:18-alpine

WORKDIR /app

# Copy package files
COPY package*.json ./
RUN npm install

# Copy source code
COPY . .

# Create environment file with your MongoDB Atlas connection
RUN echo "MONGODB_URI=mongodb+srv://aadhithyam8:Aadhi@cluster0.g1a53mc.mongodb.net/tutorialdb?retryWrites=true&w=majority" > .env
RUN echo "PORT=8080" >> .env

# Install only production dependencies
RUN npm install --only=production

EXPOSE 8080

CMD ["npm", "start"]