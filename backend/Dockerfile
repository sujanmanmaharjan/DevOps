FROM node:14.16.0-alpine3.13

WORKDIR /app
COPY package*.json ./
RUN npm install
RUN npm install pm2 -g 
RUN npm install serve -g
COPY . . 

EXPOSE 3001 

CMD ["pm2", "start" "index.js"]