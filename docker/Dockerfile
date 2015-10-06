FROM dousto/redact-box
MAINTAINER "Doug Stoeckmann" <dousto@gmail.com>
ENV container docker

RUN apt-get install -y \
    git \
    ; \
    git clone -b test-branch https://github.com/dousto/redact.git \
    && cd /redact; npm install; \
    apt-get purge -y \
    git \
    ; \
    apt-get autoremove -y

EXPOSE 7328
CMD ["node", "/redact/bin/www"]