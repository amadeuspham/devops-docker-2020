# Final image size 130MB
FROM node:alpine as build-stage

WORKDIR /usr/src/app 

COPY . .

RUN rm -rf /var/lib/apt/lists/*  && \
	npm install && \
	npm run build

FROM nginx
COPY --from=build-stage /usr/src/app/dist /usr/share/nginx/html
