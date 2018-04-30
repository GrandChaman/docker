FROM debian

RUN useradd -m teamspeak
RUN su teamspeak
RUN apt-get update && apt-get install wget -y
RUN wget http://dl.4players.de/ts/releases/3.0.11.2/teamspeak3-server_linux-amd64-3.0.11.2.tar.gz
RUN tar -zxvf teamspeak3-server_linux-amd64-3.0.11.2.tar.gz
RUN rm teamspeak3-server_linux-amd64-3.0.11.2.tar.gz

EXPOSE 9987/udp
EXPOSE 10011/tcp
EXPOSE 30033/tcp

ENTRYPOINT ["sh", "/teamspeak3-server_linux-amd64/ts3server_minimal_runscript.sh", "createinfile=1"]

