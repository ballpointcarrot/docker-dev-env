FROM phusion/baseimage

RUN rm -f /etc/service/sshd/down
ADD ../bpc.pub /tmp/bpc.pub
RUN cat /tmp/bpc.pub >> /root/.ssh/authorized_keys && rm -f /tmp/bpc.pub

RUN apt-get update && apt-get -y install python sudo
