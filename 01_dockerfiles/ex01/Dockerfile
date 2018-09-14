FROM debian:latest

EXPOSE 9987/udp 10011 30033

RUN apt-get update -y && \
	apt-get upgrade -y && \
	apt-get install wget bzip2 -y && \
	wget http://dl.4players.de/ts/releases/3.3.1/teamspeak3-server_linux_amd64-3.3.1.tar.bz2 && \
	tar -xvjf teamspeak3-server_linux_amd64-3.3.1.tar.bz2

ENTRYPOINT teamspeak3-server_linux_amd64/ts3server_minimal_runscript.sh

#docker run -it --rm -p 9987:9987/UDP -p 10011:10011/TCP -p 30033:30033/TCP -e TS3SERVER_LICENSE=accept ts
