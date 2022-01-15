FROM python:3.8-alpine
RUN \
 apk add --no-cache --virtual .build-deps gcc musl-dev openssl-dev && \
 pip install athenacli==1.6.3 && \
 apk --purge del .build-deps
RUN mkdir /out
VOLUME [ "/out" ]
RUN mkdir /in
VOLUME [ "/in" ]
ENTRYPOINT ["athenacli"]
