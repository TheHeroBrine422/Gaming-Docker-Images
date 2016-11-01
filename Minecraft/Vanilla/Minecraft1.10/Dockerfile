FROM debian:wheezy
MAINTAINER Caleb Jones <caleb@calebgj.io>
RUN apt-get -y update
RUN apt-get -y install openjdk-7-jre-headless wget
RUN wget -q https://launcher.mojang.com/mc/game/1.10.2/server/3d501b23df53c548254f5e3f66492d178a48db63/server.jar
WORKDIR /data
VOLUME /data
EXPOSE 25565
CMD echo eula=true > /data/eula.txt && java -jar /minecraft_server.1.9.jar
ADD ops.json /data
ADD whitelist.json /data
ADD server.properties /data
