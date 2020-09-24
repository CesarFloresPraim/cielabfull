# base image
FROM node:12.2.0-alpine

# Create a directory where our app will be placed
RUN mkdir -p /usr/src/app

# Change directory so that our commands run inside this new directory
WORKDIR /usr/src/app

# Copy dependency definitions
COPY package.json /usr/src/app/package.json

# Install dependecies
RUN npm install

# Get all the code needed to run the app
COPY . /usr/src/app
RUN npm install @vue/cli@3.7.0 -g

EXPOSE 80
# start app
CMD ["npm", "run", "serve"]