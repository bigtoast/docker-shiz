FROM bigtoast/java8

MAINTAINER Andrew Headrick "github.com/bigtoast"

RUN wget https://download.elasticsearch.org/logstash/logstash/logstash-1.4.2.tar.gz

RUN tar -xvzf logstash-1.4.2.tar.gz && mv logstash-1.4.2 /logstash && rm logstash-1.4.2.tar.gz && chmod -R 777 /logstash

RUN apt-get -y install ruby telnet wget

VOLUME ["/var/log", "/tmp/logstash"]

EXPOSE 9292

CMD /logstash/bin/logstash -f /tmp/logstash/logstash.conf web