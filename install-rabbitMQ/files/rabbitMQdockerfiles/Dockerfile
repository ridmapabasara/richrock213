FROM rabbitmq

# Define environment variables.
ENV RABBITMQ_USER sensu
ENV RABBITMQ_PASSWORD 1992

ADD init.sh /init.sh
ADD cacert.pem /etc/rabbitmq/ssl/cacert.pem
ADD cert.pem /etc/rabbitmq/ssl/cert.pem
ADD key.pem /etc/rabbitmq/ssl/key.pem
ADD rabbitmq.config etc/rabbitmq/rabbitmq.config

EXPOSE 15672/tcp 25672/tcp 4369/tcp 5671/tcp 5672/tcp

# Define default command
CMD ["/init.sh"]