#
# garethhowell/docker-multimarkdown-pandoc
#
# This is an image with a pandoc, calibre, multimarkdown installation.
# The image builds on the work donw by Thomas Weise - specifically, it uses
# https://github.com/thomasweise/docker-pandoc-calibre/ as its base image.
# Source: https://github.com/garethhowell/docker-multimarkdown-pandoc/
# License: GNU GENERAL PUBLIC LICENSE, Version 3, 29 June 2007
# The license applies to the way the image is built, while the
# software components inside the image are under the respective
# licenses chosen by their respective copyright holders.

FROM thomasweise/docker-pandoc-calibre
LABEL Maintainer="Gareth Howell <gareth.howell@gmail.com>"

RUN echo "Initial Update." &&\
    apt-get update &&\
    echo "Installing git." &&\
    apt-get install -f -y --no-install-recommends build-essential git cmake &&\
    cd  /tmp/ &&\
# install MultiMarkdown
    echo "Installing MultiMarkdown-6" &&\
    git clone https://github.com/fletcher/MultiMarkdown-6.git &&\
    cd MultiMarkdown-6 &&\
    make &&\
    cd build &&\
    make install &&\
    echo "Final cleanup." &&\
    apt-get clean -y &&\
    rm -rf /tmp/* /var/tmp/* &&\
    rm -rf /var/lib/apt/lists/* &&\
    rm -f /etc/ssh/ssh_host_* &&\
    find /usr/share/doc -depth -type f ! -name copyright -delete &&\
    find /usr/share/doc -type f -name "*.pdf" -delete &&\
    find /usr/share/doc -type f -name "*.gz" -delete &&\
    find /usr/share/doc -type f -name "*.tex" -delete &&\
    find /usr/share/doc -type d -empty -delete &&\
    rm -rf /usr/share/man &&\
    mkdir -p /usr/share/man &&\
    mkdir -p /usr/share/doc &&\
    echo "All done."


