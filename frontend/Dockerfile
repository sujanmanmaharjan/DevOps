FROM node:14.16.0-alpine3.13


WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build
RUN npm install pm2 -g 
RUN npm install serve -g

EXPOSE 3000 

CMD ["pm2", "serve", "build", "3000"]