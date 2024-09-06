FROM mongo:latest
ENV MONGO_INITDB_ROOT_USERNAME=admin
ENV MONGO_INITDB_ROOT_PASSWORD=password
COPY *.js /docker-entrypoint-initdb.d/
EXPOSE 27017
CMD ["mongod"]