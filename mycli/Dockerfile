FROM python:3.14-alpine
RUN /usr/local/bin/python -m pip install --upgrade pip
RUN \
 apk add --no-cache --virtual .build-deps gcc musl-dev libffi-dev openssl-dev python3-dev cargo && \ 
 pip install mycli==2.24.5 && \
 apk --purge del .build-deps
RUN mkdir /out
VOLUME [ "/out" ]
ENTRYPOINT ["mycli"]
