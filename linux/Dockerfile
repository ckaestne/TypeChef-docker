FROM ckaestne/typechef-kconfig

RUN apt-get -y update && apt-get install -y git-core gcc make

ADD https://github.com/ckaestne/TypeChef-LinuxAnalysis2/archive/master.tar.gz linuxa2.tar.gz
RUN tar xfz linuxa2.tar.gz; rm linuxa2.tar.gz; mv TypeChef-LinuxAnalysis2-master LinuxAnalysis2; cd LinuxAnalysis2; sbt mkrun

