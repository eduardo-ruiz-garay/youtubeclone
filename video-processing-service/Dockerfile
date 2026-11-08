# Use an official Node Runtime as parent image
FROM node:18

# Set working directory
WORKDIR /app

# Copy package json into working directory
COPY package*.json ./

# Install dependancies
RUN apt-get update && apt-get install -y ffmpeg

RUN npm install

COPY . . 

EXPOSE 3000

CMD [ "npm", "start" ]