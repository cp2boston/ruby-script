FROM ruby:2.2.0
MAINTAINER Fiona Hasanaj

# install necessary software
RUN apt-get -y update && apt-get install -y vim  && apt-get install -y git && gem install rubysl-securerandom

RUN mkdir /ruby
WORKDIR /ruby
COPY run_ruby.sh run_ruby.sh
RUN chmod 0755 run_ruby.sh

# allow interactive bash inside docker container
CMD ./run_ruby.sh $API_KEY $FILENAME $ALT_URL 

VOLUME ["/source"]
