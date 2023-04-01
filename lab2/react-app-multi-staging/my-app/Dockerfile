FROM node:alpine AS builder

WORKDIR /App

COPY package.json /App/
RUN npm install 
COPY . /App/


 RUN npm run build



FROM nginx:alpine

WORKDIR /usr/share/nginx/html

RUN rm -rf ./*

COPY --from=builder /App/build .

ENTRYPOINT ["nginx", "-g", "daemon off;"]
