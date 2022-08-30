# Base Image
FROM node:16

# create app directory
WORKDIR /usr/src/app

# Install app dependencies
# npm version <= 4 will not generate package-lock.json
# uses a wildcard to ensure both package.json and package-lock.json are copied where available (npm@5+)
COPY package*.json ./

# If you are building for production,
# RUN npm ci --only=production
RUN npm install 

# bundle app source
COPY . .

# expose the port bound to by the app. for docker daemon
EXPOSE 8080

# cmd to run app
CMD [ "node", "index.js" ]