FROM debian:wheezy
MAINTAINER Caleb Jones <caleb@calebgj.io>
WORKDIR /Mine10
RUN apt-get -y update
RUN apt-get -y install openjdk-7-jre-headless wget
RUN wget -q https://launcher.mojang.com/mc/game/1.10.2/server/3d501b23df53c548254f5e3f66492d178a48db63/server.jar
WORKDIR Mine10/data
VOLUME Mine10/data
EXPOSE 25565
RUN useradd mine10
RUN chown -R mine10:mine10 /Mine10
USER mine10
CMD echo eula=true > /data/eula.txt && java -jar /minecraft_server.1.9.jar
ADD ops.json /data
ADD whitelist.json /data
ADD server.properties /data
