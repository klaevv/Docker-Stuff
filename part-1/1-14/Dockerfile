FROM ruby:2.6.0

RUN curl -sL https://deb.nodesource.com/setup_10.x | bash && apt install -y nodejs

COPY . .

RUN gem install bundler && bundle install && rails db:migrate

CMD [ "rails", "s" ]
