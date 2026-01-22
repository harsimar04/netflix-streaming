FROM node:18-alpine

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .
RUN npm run build

# Install a lightweight SPA server
RUN npm install -g serve

EXPOSE 8080

# -s enables SPA fallback (fixes refresh 404)
CMD ["serve", "-s", "dist", "-l", "8080"]

