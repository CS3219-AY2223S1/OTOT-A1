# build from node v18.8.0
FROM node:18.8.0

# create app directory
WORKDIR /usr/src/app

# install app dependencies
COPY package*.json ./
RUN npm install

# bundle app source
COPY . .

# expose port for mapping
EXPOSE 8080

# run app
CMD [ "node", "index.js" ]
