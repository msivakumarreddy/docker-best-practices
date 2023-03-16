FROM node:14-alpine AS builder
WORKDIR /opt/server
COPY package.json /opt/server/
RUN npm install
RUN ls -lrt

# FROM node:14

# EXPOSE 8080

# WORKDIR /opt/server

# COPY package.json /opt/server/

# RUN npm install

# COPY server.js /opt/server/

# CMD ["node", "server.js"]

