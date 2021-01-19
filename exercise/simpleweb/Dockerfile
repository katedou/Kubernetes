# specify a base image
# alpine images does not have npm insatlled
# Alpine is a term in the docker world for an image that is as small and compact as possible.
FROM node:alpine
WORKDIR /usr/app

# Install some dependencies 
COPY ./package.json ./
RUN npm install 
COPY ./ ./

# Default command
CMD ["npm","start"]
