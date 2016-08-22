#
# Profanity ncurses based XMPP client
# http://www.profanity.im/
# github: https://github.com/boothj5/profanity
#
# This is an unofficial Dockerfile of the above project
# https://github.com/truedays/dockerfiles
#

FROM alpine

RUN apk update && \
apk add autoconf && \
apk add automake && \
apk add build-base && \
apk add curl-dev && \
apk add expat && \
apk add expat-dev && \
apk add gcc && \
apk add git && \
apk add glib && \
apk add glib-dev && \
apk add gpgme && \
apk add gpgme-dev && \
apk add libcurl && \
apk add libnotify && \
apk add libnotify-dev && \
apk add libotr && \
apk add libotr-dev && \
apk add libtool && \
apk add libuuid && \
apk add libxscrnsaver-dev && \
apk add make && \
apk add ncurses && \
apk add ncurses-dev && \
apk add openssl-dev && \
apk add readline-dev && \
mkdir /build; cd /build && \
git clone https://github.com/boothj5/libmesode.git && \
git clone https://github.com/boothj5/profanity.git && \
cd libmesode/ && \
./bootstrap.sh  && \
./configure --prefix=/usr && \
make && \
make install  && \
cd ../profanity/ && \
./bootstrap.sh  && \
./configure --prefix=/usr && \
make && \
make install && \
cd / && \
rm -rfv /build

#ENTRYPOINT ["/usr/bin/profanity"]
CMD ["/usr/bin/profanity"]
