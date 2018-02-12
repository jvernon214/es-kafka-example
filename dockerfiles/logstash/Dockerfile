FROM docker.elastic.co/logstash/logstash:6.2.0
MAINTAINER Jake Vernon	"jake.vernon@elastic.co"

COPY src /tmp/src

USER root

RUN yum -y install epel-release && yum -y update && \
   yum -y install vim nmap-ncat curl awscli jq && \
   chmod 755 /tmp/src/load_data.sh && \
   rm -f /tmp/*.zip /tmp/*.gz && \
   echo "xpack.monitoring.enabled: false" >> /usr/share/logstash/config/logstash.yml

CMD ["/tmp/src/load_data.sh"]