FROM node:14

EXPOSE 8080

WORKDIR /opt/server
RUN addgroup --system cart && adduser --system cart -G cart
RUN chown -R cart:cart /opt/server
USER cart

COPY package.json /opt/server/

RUN npm install

COPY server.js /opt/server/

CMD ["node", "server.js"]

