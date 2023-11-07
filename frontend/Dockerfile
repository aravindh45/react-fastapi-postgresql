FROM node:16.14.2 as build

WORKDIR /app


COPY . .
RUN npm i

RUN npm run build

FROM ngnix:latest

COPY --from=build /app/build /etc/nginix/html