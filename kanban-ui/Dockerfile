### STAGE 1: Build ###
<<<<<<< HEAD
FROM node:12.7-alpine AS build
=======
FROM node AS build
>>>>>>> 4bb849bb53abb1a456b0853da0974e4bd7e44640
WORKDIR /usr/src/app
COPY package.json ./
RUN npm install
COPY . .
RUN npm run build

### STAGE 2: Run ###
FROM nginx:1.17.1-alpine
COPY default.conf /etc/nginx/conf.d/default.conf
COPY --from=build /usr/src/app/dist/kanban-ui /usr/share/nginx/html
EXPOSE 80