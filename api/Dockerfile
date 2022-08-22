#this is the parent image that we're pulling from the docker hub.
FROM node:17-alpine

WORKDIR /app

# COPY src dest >>>> src is only . since we're copying from the same directory
# destination is also . since we're copying to the root dir of the image we're creating
# we can say ./blabla to create a folder called blabla inside the image we're creating
COPY . .

# we need to run npm install to install the dependecies
# RUN is used for build time.
RUN npm install

EXPOSE 4000
# required for docker desktop port mapping

# CMD is used for run time.
CMD ["node", "app.js"]