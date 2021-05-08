FROM ubuntu:16.04

RUN apt-get update \
        && apt-get --yes install python3 python3-pip \
        && apt-get --yes autoremove \
        && apt-get --yes autoclean

COPY requirements.txt /server/

RUN /usr/bin/pip3 --disable-pip-version-check install --requirement /server/requirements.txt

RUN /bin/sh -c "mkdir /db"

ENV LC_ALL=C.UTF-8 \
    LANG=C.UTF-8 \
    FLAGS_DATABASE="/db/flags.sqlite"
    
WORKDIR /server

COPY . ./

CMD /bin/sh ./start_server.sh

#CMD cd /server && /bin/sh ./start_server.sh
