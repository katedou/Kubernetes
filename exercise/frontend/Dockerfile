FROM node:alpine
WORKDIR '/app'
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build

### now for the second phase
#### /app/build <-- all the stuff been copy overed to

FROM nginx 
## Elastic Beanstalk will look at this expose
EXPOSE 80
## --from specify from which former builder to copy
## look at the https://hub.docker.com/_/nginx about the directory to put the content
COPY --from=0 /app/build /usr/share/nginx/html
### start nginx, this the nginx package will take care of it