FROM node:alpine

# create the dir inside the container
WORKDIR /usr/src/app

# copy package.json files from local machine to workdir in the container
COPY package*.json ./

# run npm install in our local machine
RUN npm install

# copy the generated modules and all other file to the container
COPY . .

EXPOSE 5000

CMD ["node", "index.js"]
