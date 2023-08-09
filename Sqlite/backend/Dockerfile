FROM jitesoft/sqlite
COPY database.db /var/lib/sqlite/

FROM node:18
WORKDIR /app
COPY package*.json ./
RUN npm install
RUN npm install -g npm@latest
COPY . .
EXPOSE 5001
CMD ["node", "app.js"]