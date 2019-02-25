FROM library/odoo:12.0
LABEL maintainer="Alistek <info@alistek.com>"

USER root

RUN set -x; \
        apt-get update \
        && apt-get upgrade -y \
        && apt-get install -y --no-install-recommends \
            git \
        && pip3 install git+https://github.com/aeroo/aeroolib.git \
        && pip3 install git+https://github.com/aeroo/currency2text.git \
        && apt-get autoremove -y \
        && apt-get clean -y

USER odoo
