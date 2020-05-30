FROM sebp/elk:750

# add plugin for logstash (beat inputs)
WORKDIR ${LOGSTASH_HOME}
RUN gosu logstash bin/logstash-plugin install logstash-input-beats

# add default configuration into docker image
COPY logstash/02-beats-input.conf /etc/logstash/conf.d/02-beats-input.conf
COPY logstash/30-output.conf /etc/logstash/conf.d/30-output.conf