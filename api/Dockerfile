# Base image we are gonna be building
FROM node:20-alpine

# set up a current working directory for docker
WORKDIR /user/src/app

# copy all of the package*json files into WORKDIR folder
COPY package*.json ./

# install all dependencies skip devproduction... this what we use in productions
RUN npm ci --only=prodcution

# copy all of the file
COPY . .

# when the container starts this will run
CMD [ "npm","run", "start:dev" ]