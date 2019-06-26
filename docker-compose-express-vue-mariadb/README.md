
  client:
    image: node:latest
    container_name: vue
    working_dir: /usr/src/service/client
    volumes:
      - ./client/node_modules:/usr/src/service/client/node_modules
      - ./client:/usr/src/service
    environment:
      - NODE_ENV=${NODE_ENV}
    command: npm run serve
    ports:
      - ${VUE_PORT}:8080