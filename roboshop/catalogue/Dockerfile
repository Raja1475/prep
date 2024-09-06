FROM node:14

# Set the working directory inside the container
WORKDIR /app

# Copy the package.json file to the container
COPY package.json .

# Install the Node.js dependencies
RUN npm install

# Copy the server.js file to the container
COPY server.js .

# Expose the port your app will run on
EXPOSE 8080

# Start the application
CMD ["node", "server.js"]
