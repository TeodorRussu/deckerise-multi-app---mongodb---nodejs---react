FROM node

WORKDIR /app

COPY package.json ./

RUN npm install

COPY . ./

ENV PORT 80

ENV MONGO_CONNECTOR 'mongodb://host.docker.internal:27017/course-goals'

EXPOSE 80

CMD ["node", "app.js"]

#mongodb
# docker run -p 27017:27017 --name mongo_db mongo:latest

# docker build node_app_backend  .
# docker run -d  --env PORT=80 --env MONGO_CONNECTOR=mongodb://host.docker.internal:27017/course-goals -p 80:80 --name node_backend  node_app_backend:latest