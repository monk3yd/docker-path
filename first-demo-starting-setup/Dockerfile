# base image
FROM node:14

# special directory in container filesystem in which to work
WORKDIR /app

# Copy package.json file into working directory
COPY package.json .

# Run npm for installing all depedencies our app needs
RUN npm install

# Copy rest of the code in app folder
COPY . .

# Expose port 3000 to outside world for connection to outside of container
EXPOSE 3000

# execute app.mjs file with the node command
CMD [ "node", "app.mjs" ]
