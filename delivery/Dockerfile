FROM alpine

RUN apk add --update ca-certificates

COPY bin/delivery /usr/bin/delivery

EXPOSE 5001

ENTRYPOINT [ "delivery" ]
