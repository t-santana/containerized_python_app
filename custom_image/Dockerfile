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

RUN apt-get update && apt-get install python=3.9 python=3.9-dev -y --no-install-recommends ;\
	rm -rf /var/lib/apt/lists/*

RUN apt-get update && apt-get install python3-pip -y --no-install-recommends ;\
	rm -rf /var/lib/apt/lists/*

RUN ln -s /usr/bin/python3 /usr/bin/python

CMD [ "python" ]
