FROM ckaestne/typechef-kconfig

RUN apt-get -y update && apt-get install -y git-core gcc make

ADD https://github.com/ckaestne/TypeChef-BusyboxAnalysis/archive/master.tar.gz busyboxa.tar.gz
RUN tar xfz busyboxa.tar.gz; mv TypeChef-BusyboxAnalysis-master BusyboxAnalysis; cd BusyboxAnalysis; sbt publish-local

ADD https://github.com/ckaestne/TypeChef-BusyboxAnalysis2/archive/master.tar.gz busyboxa2.tar.gz
RUN tar xfz busyboxa2.tar.gz; rm busyboxa2.tar.gz; mv TypeChef-BusyboxAnalysis2-master BusyboxAnalysis2; cd BusyboxAnalysis2; sbt mkrun

#CMD /usr/games/fortune -a
