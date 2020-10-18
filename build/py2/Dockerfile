FROM python:2

RUN mkdir /event
WORKDIR /event
COPY ../../python-api ./python-api/
COPY requirements.txt ./
RUN /usr/local/bin/python -m pip install --upgrade pip
RUN pip install --no-cache-dir -r requirements.txt
CMD [ "python", "/event/shotgunEventDaemon.py","foreground" ]
