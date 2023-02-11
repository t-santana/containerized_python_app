FROM debian:11-slim

ENV LANG C.UTF-8

RUN set -eux; \
	apt-get update; \
	apt-get install -y --no-install-recommends \
    ca-certificates \
		netbase \
		tzdata \
        ; \
        rm -rf /var/lib/apt/lists/*

RUN apt-get update && apt-get install -y python3.9 python3.9-dev
RUN apt-get update && apt-get install python3-pip -y
RUN ln -s /usr/bin/python3 /usr/bin/python

WORKDIR /usr/src/app

COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

ENTRYPOINT [ "python", "./python_app.py", "--lines_number" ]
