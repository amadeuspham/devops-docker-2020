FROM ubuntu:16.04 

WORKDIR /usr/src/app 

ENV FRONT_URL=http://localhost:5000

RUN useradd -m harry && \
	chown harry -R /usr/src/app && \
	apt-get update && apt-get install -y \
	curl && \
	curl -sL https://deb.nodesource.com/setup_10.x | bash && \
	apt-get install -y nodejs && \
	apt-get purge -y --auto-remove curl && \
	rm -rf /var/lib/apt/lists/* 

COPY package.json .

RUN npm install
COPY . .

EXPOSE 8000

CMD ["npm","start"]