FROM redhat/ubi8:latest

USER root

ENV TOMCAT_VERSION 9.0.64
ENV IIQ_VERSION 8.3
ENV OpenJDK_Version 11.0.15

# Fix sh
RUN rm /bin/sh && ln -s /bin/bash /bin/sh

# Install Zip & Unzip, #yum install for redhat packages, refer to base.yml
RUN yum install zip unzip -y && \
yum install java-11-openjdk -y 

# Copy Files from Artifacts #copy from base path to /tmp path
COPY ./apache-tomcat-${TOMCAT_VERSION}.tar.gz /tmp

# Create Directories, \ = newline
RUN mkdir /software && \
mkdir /software/tomcat

# Unzip and move
RUN tar -xvf /tmp/apache-tomcat-${TOMCAT_VERSION}.tar.gz -C /software && \
cp -r /software/apache-tomcat-${TOMCAT_VERSION}/* /software/tomcat

# Clean up
RUN rm -rf /tmp/apache-tomcat-${TOMCAT_VERSION}.tar.gz && \
rm -rf /software/apache-tomcat-${TOMCAT_VERSION}

RUN chmod -R 775 /software

#ENV JAVA_HOME="/software/java"
#ENV JDK_HOME="/software/java"
#ENV PATH="/software/jdk-java/bin:$PATH"

# Launch IIQ (Testing Purposes)
CMD ["/software/tomcat/bin/catalina.sh", "run"]