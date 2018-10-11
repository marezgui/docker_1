FROM ruby 

ONBUILD COPY app /opt/app
ONBUILD WORKDIR /opt/app

ONBUILD RUN apt-get update \
		&& apt-get install nodejs -y \ 
		&& bundle install \
		&& rake db:migrate \
		&& rake db:seed 
