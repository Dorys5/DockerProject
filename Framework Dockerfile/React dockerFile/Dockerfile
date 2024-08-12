# étape de build
FROM node:lts-alpine as build-stage
WORKDIR /app
COPY package*.json ./
RUN npm install -g serve
RUN npm install
COPY . .
RUN npm run build

# étape de production

EXPOSE 3000
CMD ["serve", "-s", "build"]