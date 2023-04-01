FROM node 

WORKDIR /App

COPY package.json /App/
RUN npm install 
COPY . /App/

ENTRYPOINT [ "npm","start" ]
