FROM docker.elastic.co/beats/filebeat:6.2.0
MAINTAINER Jake Vernon "jake.vernon@elastic.co"

USER root

RUN chown filebeat /usr/share/filebeat/filebeat.yml && \
	yum -y install epel-release && yum -y update && \
	yum -y install vim nmap-ncat curl awscli jq telnet

USER filebeat