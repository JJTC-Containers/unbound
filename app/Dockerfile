FROM alpine:edge

LABEL maintainer JJTC "docker@jjtc.eu"

COPY docker-entrypoint.sh /docker-entrypoint.sh

RUN apk update \
  && apk add --no-cache drill libressl unbound \
	&& ./etc/periodic/monthly/update-unbound-root-hints \
	&& chown root:unbound /etc/unbound \
  && adduser unbound tty \
	&& chmod 775 /etc/unbound \
  && chmod +x /docker-entrypoint.sh

EXPOSE 53/udp 53/tcp

ENTRYPOINT ["/docker-entrypoint.sh"]
CMD [ "unbound" ]
