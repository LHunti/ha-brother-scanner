FROM sbs20/scanservjs:latest 
# Current v3.0.4

USER root

# Brother brscan4 illesztőprogram letöltése és telepítése közvetlenül a gyártótól
RUN apt-get update && apt-get install -y wget \
    && wget https://download.brother.com/welcome/dlf105200/brscan4-0.4.11-1.amd64.deb -O /tmp/brscan.deb \
    && dpkg -i /tmp/brscan.deb \
    && echo "brother4" >> /etc/sane.d/dll.conf \
    && rm /tmp/brscan.deb \
    && apt-get clean
