# FROM node:20
#IC-1
FROM node:20.18.3-alpine3.21 AS builder
     
#install bash
WORKDIR /opt/backend
COPY package.json ./
COPY *.js ./
#install depencies
RUN npm install


FROM node:20.18.3-alpine3.21
RUN addgroup -S expense && adduser -S expense -G expense && \
     mkdir /opt/backend && \
     chown -R expense:expense /opt/backend
ENV DB_HOST="mysql"
# ENV DB_HOST="localhost"
WORKDIR /opt/backend
USER expense
COPY --from=builder /opt/backend /opt/backend
CMD ["node","index.js"]