FROM node:14.16.0-alpine3.13
# RUN mkdir node_modules/.cache && chmod -R 777 node_modules/.cache

RUN addgroup app && adduser -S -G app app
USER app

WORKDIR /app
# RUN chown -R app /app
COPY package*.json ./
RUN npm install
COPY . .

EXPOSE 3000 

CMD ["npm", "start"]