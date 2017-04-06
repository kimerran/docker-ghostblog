FROM alpine:latest
WORKDIR /var/www
COPY ghost.zip /var/www
COPY config.js /var/www

RUN apk update
RUN apk add nodejs

RUN unzip ghost.zip -d /var/www

RUN npm install --production

EXPOSE 2368

ENTRYPOINT ["npm","start","--production"]
