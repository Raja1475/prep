FROM node:14
EXPOSE 8080
WORKDIR /app
RUN cd /app
COPY package.json .
RUN npm install
COPY server.js .
CMD [ "node", "server.js" ]
