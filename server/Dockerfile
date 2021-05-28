FROM alpine

RUN apk add py3-pip

COPY requirements.txt /server/

RUN /usr/bin/pip3 install --upgrade --force-reinstall setuptools==45.3.0 \
    && /usr/bin/pip3 --disable-pip-version-check install --requirement /server/requirements.txt

RUN /bin/sh -c "mkdir /db"

ENV LC_ALL=C.UTF-8 \
    LANG=C.UTF-8 \
    FLAGS_DATABASE="/db/flags.sqlite"
    
WORKDIR /server

COPY . ./

RUN rm -rf Dockerfile

CMD /bin/sh ./start_server.sh
