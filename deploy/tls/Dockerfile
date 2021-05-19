FROM alpine:3.13
ENTRYPOINT [ "/entrypoint.sh" ]

RUN sed -i 's/https/http/' /etc/apk/repositories
RUN apk add --no-cache --update --upgrade ca-certificates postgresql-client
RUN sed -i 's/http/https/' /etc/apk/repositories
RUN apk add --no-cache --update --upgrade --repository=http://dl-cdn.alpinelinux.org/alpine/edge/testing cfssl

COPY . .
