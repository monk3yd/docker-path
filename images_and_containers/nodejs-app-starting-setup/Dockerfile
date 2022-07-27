# Dockerfile contains the instructions for docker that we want to exec
# when building a container from our own image

# --- Setting up image template (Code runs when building/creating image)
# 1. (FROM) Import base image into own image
FROM node

# 2. (WORKDIR) Set working directory of docker container
# All subsequent commands will be executed from inside of workdir (folder)
WORKDIR /app

# 3. (COPY) Select files from local that should go into own image
# first dot: all dirs, subdirs and files on local project should be copied into own image
# second dot: path inside own image filesystem where those dirs & files should be stored
# good idea not to use root folder ., instead use /app in this case (name whatever you want, if it doesn't exist it is created)
COPY . /app

# 4. (RUN) Install dependencies in workdir of application by running commands
# By default the workdir of the app is /root
RUN npm install

# 5. (EXPOSE) Let docker know to open given port for outside communication (documentation purpose, needs to open port when running container)
EXPOSE 80

# --- Code that runs when a container starts
# 6. (CMD)
CMD ["node", "server.js"]
