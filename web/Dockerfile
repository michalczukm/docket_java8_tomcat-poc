FROM tomcat:9-jre8
LABEL Author="michalczukm"

RUN alias ll='ls -lsha'
RUN apt install vi || apt install nano
RUN echo "export JAVA_OPTS=\"-Dapp.env=staging\"" > /usr/local/tomcat/bin/setenv.sh  
COPY ./application.war /usr/local/tomcat/webapps/ROOT.war


CMD ["catalina.sh", "run"]