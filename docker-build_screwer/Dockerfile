FROM ubuntu:16.04

RUN apt-get update \
	&& apt-get -y install \
		aptitude \
		wget ftp man rsync \
		zsh vim multitail \
		tcpdump netcat nmap \
		iotop iftop \
		gawk gcc make automake git \
	&& rm -rf /var/lib/apt/lists/*

COPY locale.gen /etc/locale.gen
COPY .zkbd /root/.zkbd
COPY .zshrc /root/.zshrc
COPY .vimrc /root/.vimrc
COPY .aliases /root/.aliases
RUN locale-gen

ENV LANG en_US.UTF-8
ENV LANGUAGE en_US:en
ENV LC_ALL en_US.UTF-8

VOLUME /share

CMD ["/usr/bin/zsh"]
