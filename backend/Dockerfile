FROM node:20
#install bash
WORKDIR /opt/backend
COPY package.json .
COPY *.js .
#install depencies
RUN npm install
ENV DB_HOST="mysql"
# ENV DB_HOST="localhost"
CMD ["node","index.js"]