FROM ibmcom/mq

COPY *.sh /usr/local/bin/
COPY *.mqsc /etc/mqm/

COPY mq-dev-config /etc/mqm/mq-dev-config

RUN chmod +x /usr/local/bin/*.sh

# Always use port 1414 (the Docker administrator can re-map ports at runtime)
# Expose port 9443 for the web console
EXPOSE 1411 9443

ENV LANG=en_US.UTF-8

ENTRYPOINT ["mq.sh"]
