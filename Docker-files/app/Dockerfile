FROM openjdk:11 AS JDK_Image
LABEL "Project"="ProfileApp"
LABEL "Author"="Owais"
RUN apt update && apt install -y maven 
RUN git clone https://github.com/devopshydclub/vprofile-project.git 
RUN cd vprofile-project && git checkout docker && mvn clean install


FROM tomcat:9-jre11
RUN rm -rf /usr/local/tomcat/webapps/*
COPY --from=JDK_Image /vprofile-project/target/vprofile-v2.war /usr/local/tomcat/webapps/ROOT.war

EXPOSE 8080
CMD ["catalina.sh", "run"]

