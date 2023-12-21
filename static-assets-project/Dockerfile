# build stage
FROM node:latest AS builder
WORKDIR /app
COPY . .
RUN npm ci
RUN npm run build

# runtime stage
FROM nginx:latest
COPY --from=builder /app/build /usr/share/nginx/html
