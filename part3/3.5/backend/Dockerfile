FROM node:alpine

WORKDIR /usr/src/app 

ENV FRONT_URL=http://localhost:5000

RUN chown node -R /usr/src/app && \
	rm -rf /var/lib/apt/lists/* 

COPY package.json .

RUN npm install
COPY . .

EXPOSE 8000

CMD ["npm","start"]