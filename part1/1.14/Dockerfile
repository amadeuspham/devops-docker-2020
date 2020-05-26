FROM ruby:2.6.0

WORKDIR /usr/src/app
RUN apt-get update && apt install -y nodejs
COPY . .

RUN gem install bundler
RUN bundle install 

RUN rails db:migrate
CMD ["rails","s"]