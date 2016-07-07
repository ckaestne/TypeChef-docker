FROM ckaestne/typechef-base

RUN apt-get -y update && apt-get install -y maven

#kbuildminer
ADD https://github.com/ckaestne/KBuildMiner/archive/master.tar.gz kbuildminer.tar.gz
RUN tar xfz kbuildminer.tar.gz; rm kbuildminer.tar.gz; mv KBuildMiner-master KBuildMiner;  cd KBuildMiner; mvn compile; mvn dependency:build-classpath -Dmdep.outputFile=.classpath-scala

#kconfigreader
ADD https://github.com/ckaestne/kconfigreader/archive/master.tar.gz kconfigreader.tar.gz
RUN tar xfz kconfigreader.tar.gz; rm kconfigreader.tar.gz; mv kconfigreader-master kconfigreader; cd kconfigreader; sbt mkrun
