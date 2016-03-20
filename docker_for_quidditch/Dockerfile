
FROM mysql:01
MAINTAINER Mohan Singh rajpootmohan@gmail.com ,Naresh Sherwal naresh.sherwal@gmail.com

# required software for quidditch app
RUN apt-get update
RUN apt-get -y install memcached nodejs ruby bundler libcurl4-openssl-dev libssl-dev

#install passenger
ENV PASSENGER_VERSION 4.0.37
RUN /bin/bash -l -c 'gem install passenger --version $PASSENGER_VERSION'
RUN /bin/bash -l -c 'passenger-install-nginx-module --auto-download --auto --prefix=/opt/nginx'
RUN mkdir -p /opt/nginx/logs
RUN touch /opt/nginx/logs/access.log
RUN touch /opt/nginx/logs/error.log
RUN ln -sf /dev/stdout /opt/nginx/logs/access.log
RUN ln -sf /dev/stderr /opt/nginx/logs/error.log

#RUN mkdir -p /usr/src/app
#WORKDIR /usr/src/app
#ADD nginx.conf /opt/nginx/conf/nginx.conf
#RUN echo "daemon off;" >> /opt/nginx/conf/nginx.conf
#ADD . /usr/src/app
#RUN bundle install --system

EXPOSE 80

CMD ["/bin/bash"]
