# Pulling parent image (node image) from docker hub
FROM node:17-alpine

# Specifying the port the container will expose
# Required for docker desktop port mapping
EXPOSE 4000

# Specifying the working directory for the image
WORKDIR /app

COPY ./package.json .
# Copying source code to the image
# The first dot represent the relative path to the source files
# The second dot is the path inside the image where we want to copy the source files
COPY . .

# Installing the dependencies in the package.json file to the image
RUN npm install

# CMD specifies any command that will be run at runtime that is when the container is running
CMD [ "node", "app.js" ]
