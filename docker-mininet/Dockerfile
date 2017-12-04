FROM ubuntu:16.04

MAINTAINER Yunjian Peng <sstriver@qq.com>

USER root
WORKDIR /root


COPY entrypoint.sh /

RUN apt-get update && apt-get install -y --no-install-recommends \
	curl \
	sudo \
	socat \
	vlc \
	iproute2 \
	iputils-ping \
	net-tools \
	tcpdump \
	nano \
	x11-xserver-utils \
	xterm \
	python \
	python-pip \
	python-setuptools \
	python-matplotlib \
	git-all \
	lsb-release \
 && rm -rf /var/lib/apt/lists/* \
 && mv /bin/ping /sbin/ping \
 && mv /bin/ping6 /sbin/ping6 \
 && mv /usr/sbin/tcpdump /usr/bin/tcpdump \
 && chmod +x /entrypoint.sh \
# && chmod -R +x ./net \
 && pip install -I networkx==1.11 \
 && pip install matplotlib

RUN git clone https://github.com/mininet/mininet
RUN chmod +x mininet/util/install.sh
RUN mininet/util/install.sh -a

EXPOSE 6640
ENTRYPOINT ["/entrypoint.sh"]
