FROM node:slim


# Setting up the work directory
WORKDIR /express-docker

# Copying all the files in our project
COPY . .

# Installing dependencies
RUN npm install

# Starting our application
CMD [ "node", "./app.js" ]

# Exposing server port
EXPOSE 3000
