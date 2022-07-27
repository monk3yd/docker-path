# Dockerfile contains the instructions for docker that we want to exec
# when building a container from our own image

# 1. (FROM) Import base image into own image
FROM node

# 2. (COPY) Select files from local that should go into own image
# first dot: all dirs, subdirs and files on local project should be copied into own image
# second dot: path inside own image where those dirs & files should be stored
COPY . .