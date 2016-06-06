FROM elasticsearch:latest
MAINTAINER swfz <sawafuji.09@gmail.com>

RUN /usr/share/elasticsearch/bin/plugin install analysis-kuromoji
RUN /usr/share/elasticsearch/bin/plugin install royrusso/elasticsearch-HQ
RUN /usr/share/elasticsearch/bin/plugin install polyfractal/elasticsearch-inquisitor

EXPOSE 9200 9300

CMD /etc/init.d/elasticsearch start && tail -f /dev/null
