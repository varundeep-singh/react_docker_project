From node:alpine as builder
WORKDIR '/app'
COPY ./package.json ./
Run npm install
COPY . .
Run npm run build


From nginx 
Expose 3000
COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf
COPY --from==builder /app/buid /usr/share/nginx/html
