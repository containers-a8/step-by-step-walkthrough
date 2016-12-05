#FROM registry.ng.bluemix.net/vabbosh/wdp-tomcat-base:6
FROM registry.ng.bluemix.net/iwinoto/wdp-tomcat-base-a8:latest
#FROM iwinoto/wdp-tomcat-base-a8:latest

ADD ROOT.war "/usr/local/tomcat/webapps/ROOT.war"
RUN rm -rf "/usr/local/tomcat/webapps/ROOT" && chown -R tomcat:tomcat /usr/local/tomcat && \
    chmod -R u+rwx /usr/local/tomcat && chmod -R go-rwx /usr/local/tomcat

######################
# Consul.io
######################
#Give tomcat user ownership of Consul data directory
#RUN chown -R tomcat:tomcat /data/consul && chmod -R u+rw /data/consul

#USER tomcat
#ENV SERVICE_NAME accounts-savingsdeposits-v1

#CMD ["/usr/local/tomcat/bin/catalina-wrapper.sh", "run"]

######################
# Amalgam8
######################
ENV A8_SERVICE=accounts-savingsdeposits:v1
CMD ["/usr/local/tomcat/bin/catalina.sh", "run"]
