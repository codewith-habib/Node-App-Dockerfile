# A Node.js Express application built with TypeScript, which serves as a web API

#Using the official Node JS Image
FROM node:latest

#Creating a WORK Directory, can name any 
WORKDIR /usr/src/app 

#Copying the Package.json file for installing npm packages
# * means, all package.json files, ./ means to working directory
COPY package*.json ./

# installing packages
RUN npm insatll
# Copying rest of all code
COPY . .

#Now for TS command, as its build with TS
RUN tsc

#Optionally we can expose it and we should to any port
EXPOSE 3000

#To start the application,as its in dist folder
CMD [ "node", "dist/index.js" ]

