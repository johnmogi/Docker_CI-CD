FROM node:14-alpine
RUN mkdir -p /home/app/node_modules && chown -R node:node /home/app
LABEL maintainer="john mogi AT johnmogi.com"

WORKDIR /home/app
ADD ./app /home/app

ENV port=8080
EXPOSE 8080
RUN npm install

CMD [ "npm", "run", "initdb" ]
ENTRYPOINT [ "npm", "run", "dev" ]