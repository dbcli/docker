FROM python:3.8-alpine
RUN /usr/local/bin/python -m pip install --upgrade pip
RUN \
 apk add --no-cache --virtual .build-deps gcc musl-dev libffi-dev openssl-dev python3-dev cargo && \ 
 pip install mycli==1.24.1 && \
 apk --purge del .build-deps
RUN mkdir /out
VOLUME [ "/out" ]
ENTRYPOINT ["mycli"]