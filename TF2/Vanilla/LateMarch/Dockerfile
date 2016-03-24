FROM fedora:latest
MAINTAINER Caleb Jones <caleb@calebgj.io>
RUN dnf -y install wget ncompress libgcc.x86_64 libgcc.i686 glibc.i686 zlib.i686 ncurses-libs.i686 tar
RUN mkdir hlserver
WORKDIR /hlserver
ADD tf2.txt /hlserver
ADD update.sh /hlserver
ADD start.sh /hlserver
RUN wget http://media.steampowered.com/installer/steamcmd_linux.tar.gz
RUN tar zxf steamcmd_linux.tar.gz
RUN rm steamcmd_linux.tar.gz
RUN chmod +x /hlserver/update.sh
RUN sh update.sh
ADD server.cfg /hlserver/tf2/tf/cfg
CMD start.sh
