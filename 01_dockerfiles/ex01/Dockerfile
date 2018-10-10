FROM debian
RUN adduser --system teamspeak \
	&& apt-get update -y \
	&& apt-get install wget bzip2 -y \
	&& wget http://dl.4players.de/ts/releases/3.4.0/teamspeak3-server_linux_amd64-3.4.0.tar.bz2 \  
	&& tar -xvf teamspeak3-server_linux_amd64-3.4.0.tar.bz2 \
	&& mv teamspeak3-server_linux_amd64 teamspeak3 \
	&& rm teamspeak3-server_linux_amd64-3.4.0.tar.bz2 \
	&& mv teamspeak3 /home/teamspeak
ENTRYPOINT sh /home/teamspeak/teamspeak3/ts3server_minimal_runscript.sh license_accepted=1 


#docker run -it -p 9987:9987/udp -p 10011:10011 -p 30033:30033
