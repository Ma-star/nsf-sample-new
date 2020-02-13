#FROM hub.c.163.com/qingzhou/nginx:v1.13.2
#EXPOSE 80

#RUN mkdir /etc/nginx/download/

#CMD ["nginx", "-g", "daemon off;"]


FROM harbor.qingzhou-test.xac.com/library/tomcat-8.5-jdk8-openjdk-skiff:v1.1-190911

#ADD target/nsf*.war /usr/local/tomcat/webapps/
ADD nsf-demo-stock-viewer/target/nsf*.war /usr/local/tomcat/webapps/

RUN cd /usr/local/tomcat/webapps && \
    mv nsf*.war ROOT.war && \
   rm -rf ROOT

CMD ["catalina.sh", "run"]