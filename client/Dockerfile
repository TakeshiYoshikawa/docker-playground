FROM node
RUN apt-get update && apt-get install -y openssl ca-certificates

WORKDIR /client

COPY package*.json /client/

RUN npm install

COPY . /client/

EXPOSE 3000

CMD ["npm", "start"]