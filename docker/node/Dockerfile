FROM node:10.16.3-alpine

# create destination directory
RUN mkdir -p /usr/src/nuxt-app
WORKDIR /usr/src/nuxt-app

# update and install dependency
RUN apk update && apk upgrade

# copy the app, note .dockerignore
COPY . /usr/src/nuxt-app/
RUN npm install && npm run build

EXPOSE 3000

## set app serving to permissive / assigned
ENV NUXT_HOST=0.0.0.0
## set app port
#ENV NUXT_PORT=3000

# start the app
CMD [ "npm", "start" ]
