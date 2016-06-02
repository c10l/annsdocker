#Set the base operating system image (iron/ruby is a minimalist ruby base image)
FROM iron/ruby

# File Author / Maintainer
MAINTAINER bob bob@example.com

RUN apk --update add ruby-rdoc ruby-irb

RUN gem install bundler

ADD /unicorn /unicorn

EXPOSE 8080

WORKDIR /unicorn

RUN bundle install

CMD bundle exec rackup --port 8080 --host 0.0.0.0

