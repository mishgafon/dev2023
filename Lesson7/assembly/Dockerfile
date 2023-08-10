FROM ubuntu:18.04
RUN apt update
RUN apt install -y maven git 
#WORKDIR /opt/tomcat
#RUN wget https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.78/bin/apache-tomcat-9.0.78.tar.gz 
#RUN tar zxf apache-tomcat-9.0.78.tar.gz
WORKDIR  /boxfuse
RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello 
WORKDIR /boxfuse/boxfuse-sample-java-war-hello
RUN mvn package
#RUN cp /boxfuse/boxfuse-sample-java-war-hello/target/hello-1.0.war /opt/tomcat/apache-tomcat-9.0.78/webapps
#EXPOSE 8080
#CMD ["/opt/tomcat/apache-tomcat-9.0.78/bin/catalina.sh", "run"]