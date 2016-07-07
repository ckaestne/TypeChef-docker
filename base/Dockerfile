FROM ubuntu:14.04
RUN echo "deb http://dl.bintray.com/sbt/debian /" | tee -a /etc/apt/sources.list.d/sbt.list
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 2EE0EA64E40A89B84B2DF73499E82A75642AC823 
RUN apt-get -y update && apt-get install -y openjdk-7-jdk sbt 
#RUN git clone https://github.com/ckaestne/KBuildMiner.git; cd KBuildMiner; mvn compile; mvn dependency:build-classpath -Dmdep.outputFile=.classpath-scala

#typechef
ADD https://github.com/ckaestne/TypeChef/archive/master.tar.gz TypeChef2.tar.gz
RUN tar xfz TypeChef2.tar.gz; mv TypeChef-master TypeChef; cd TypeChef; sbt mkrun

