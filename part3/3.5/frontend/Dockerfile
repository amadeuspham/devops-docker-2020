FROM node:alpine

WORKDIR /usr/src/app 

ENV API_URL=http://localhost:8000

RUN chown node -R /usr/src/app && \
	rm -rf /var/lib/apt/lists/* 

COPY package.json .

RUN npm install
COPY . .

EXPOSE 5000

CMD ["npm","start"]