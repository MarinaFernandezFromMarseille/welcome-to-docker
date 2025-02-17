FROM node:16-alpine

# Create app directory
WORKDIR /usr/src/app

# Copy package.json and install dependencies
COPY package.json ./
RUN npm install

# Copy the rest of the application source
COPY . .

EXPOSE 3000

CMD [ "node", "server.js" ]
