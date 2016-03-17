FROM ubuntu:14.04
MAINTAINER Mohan Singh rajpootmohan@gmail.com

#Ensuring UTF-8
RUN locale-gen en_US.UTF-8
ENV LANG       en_US.UTF-8
ENV LC_ALL     en_US.UTF-8

# Installing bunch of essentials
RUN apt-get update && apt-get -y install  sudo gcc g++ curl g++-multilib gcc-multilib \
	openssl git htop vim screen wget unzip \
	openssh-server openssh-client net-tools \
	inetutils-ping sed telnet maven

CMD ["/bin/bash"]
