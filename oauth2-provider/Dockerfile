FROM node:0.12.1

MAINTAINER Zalando SE

RUN npm install basic-auth@1.0.1
RUN npm install body-parser@1.12.4
RUN npm install express@4.12.4
RUN npm install jade@1.10.0
RUN npm install node-uuid@1.4.3

COPY /scm-source.json /
COPY /src/ /www/

WORKDIR /www/
CMD node server.js
EXPOSE 7002
