FROM debian:wheezy
MAINTAINER Caleb Jones <caleb@calebgj.io>
RUN apt-get -y update
RUN apt-get -y install openjdk-7-jre-headless wget
RUN wget -q https://s3.amazonaws.com/Minecraft.Download/versions/1.8.7/minecraft_server.1.8.7.jar
WORKDIR /data
VOLUME /data
EXPOSE 25565
CMD echo eula=true > /data/eula.txt && java -jar /minecraft_server.1.8.7.jar
ADD ops.json /data
ADD whitelist.json /data
ADD server.properties /data
