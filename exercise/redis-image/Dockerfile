#use an existing odcker image as base
From alpine
# Download and intsall dependency
Run apk add --update redis
Run apk add --update gcc

# Tell the image what to do when it starts as a container
CMD ["redis-server"]