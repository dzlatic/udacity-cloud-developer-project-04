FROM node:12
# Create app directory
WORKDIR /usr/src/app
# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
# per some findings on https://stackoverflow.com/questions/32105251/bcrypt-invalid-elf-header-with-docker-and-sails-js
COPY package*.json /usr/src/app/
RUN npm install
COPY . /usr/src/app/
# RUN npm ci 
# Bundle app source
# COPY . .
EXPOSE 8080
CMD [ "npm", "run", "prod" ]
