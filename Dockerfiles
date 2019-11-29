FROM node:6-alpine

ENV CI='true'

COPY . /app

WORKDIR /app

RUN ["npm", "install"]

RUN ["./jenkins/scripts/test.sh"]

CMD ["echo", "$PWD"]
