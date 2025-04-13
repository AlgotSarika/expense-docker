FROM node:20
#install bash
RUN apt-get update && apt-get install -y bash
WORKDIR /opt/backend
COPY package.json .
COPY *.js .
#install depencies
RUN npm install
ENV DB_HOST="mysql"
CMD ["node","index.js"]