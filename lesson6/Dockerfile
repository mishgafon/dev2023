FROM ubuntu:18.04
RUN apt update
RUN apt install -y default-jdk maven wget git 
WORKDIR /opt/tomcat
RUN mkdir -p /boxfuse
WORKDIR  /boxfuse
RUN wget https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.78/bin/apache-tomcat-9.0.78.tar.gz 
RUN tar zxf /boxfuse/apache-tomcat-9.0.78.tar.gz -C /opt/tomcat/
RUN git clone https://github.com/boxfuse/boxfuse-sample-java-war-hello 
WORKDIR /boxfuse/boxfuse-sample-java-war-hello
RUN mvn package
WORKDIR /boxfuse/boxfuse-sample-java-war-hello/target
RUN cp hello-1.0.war /opt/tomcat/apache-tomcat-9.0.78/webapps
EXPOSE 8080
CMD ["/opt/tomcat/apache-tomcat-9.0.78/bin/catalina.sh", "run"]