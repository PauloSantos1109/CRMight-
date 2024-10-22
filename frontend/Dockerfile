# Frontend Dockerfile (Nuxt.js)
FROM node:18-alpine

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

# Executa o build do Nuxt.js e exibe a saída
RUN npm run build && echo "Build successful!" || (echo "Build failed!" && exit 1)

EXPOSE 3000

CMD ["npm", "run", "start"]
