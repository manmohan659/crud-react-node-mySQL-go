FROM node:20-alpine

WORKDIR /app

COPY package*.json ./
RUN npm ci

COPY . .

EXPOSE 8800

CMD ["sh", "-c", "sed -i 's/host: \"localhost\"/host: \"db\"/' index.js && sed -i 's/password: \"\"/password: \"root\"/' index.js && node index.js"]
