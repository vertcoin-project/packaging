FROM ubuntu:20.04
RUN apt-get update
RUN apt-get -y upgrade
RUN DEBIAN_FRONTEND=noninteractive TZ=Etc/UTC apt-get -y install tzdata
RUN DEBIAN_FRONTEND=noninteractive apt-get install -y keyboard-configuration
RUN apt-get -y install build-essential libtool autotools-dev automake pkg-config bsdmainutils python3
RUN apt-get -y install ntp make g++ gcc autoconf cpp ngrep iftop sysstat
RUN apt-get -y install git wget gnupg dput dh-make dh-exec devscripts bash-completion lintian lcov html2text debhelper
RUN apt-get -y install libboost-chrono-dev libboost-filesystem-dev libboost-system-dev libboost-test-dev libboost-thread-dev
RUN apt-get -y install libevent-dev libprotobuf-dev libssl-dev protobuf-compiler
RUN apt-get -y install libzmq3-dev libsqlite3-dev libqrencode-dev libminiupnpc-dev libgmp-dev
RUN apt-get -y install qt5-qmake qtbase5-dev qttools5-dev-tools
RUN apt-get -y install libdb5.3 libdb5.3-dev libdb5.3++-dev

ENV VERSION=0.18.0
ENV DEBFULLNAME="vertion"
ENV DEBEMAIL="vertion@protonmail.com"

COPY packaging /root/

# import gpg private key, set passphrase, set as default-key and trusted-key in ~/.gnupg/gpg.conf
# edit /etc/dput.cf
    #replace [ppa] to [vertcoin-core]
    #replace incoming = ~<your_launchpad_id>/ubuntu/ to incoming = ~vertcoin-project/ubuntu/vertcoin-core