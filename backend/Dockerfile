FROM node:20-apline
#install bash
RUN apk add --no-cache bash
WORKDIR /opt/backend
COPY package.json .
COPY *.js .
#install depencies
RUN npm install
ENV DB_HOST="mysql"
CMD ["node","index.js"]