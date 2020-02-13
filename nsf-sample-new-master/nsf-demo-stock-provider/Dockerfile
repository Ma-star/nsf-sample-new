FROM harbor.qingzhou-test.xac.com/library/tomcat-8.5-jdk8-openjdk-skiff:v1.1-190911

ADD nsf-demo-stock-provider/target/nsf*.war /usr/local/tomcat/webapps/

RUN cd /usr/local/tomcat/webapps && \
    mv nsf*.war ROOT.war && \
    rm -rf ROOT

CMD ["catalina.sh", "run"]