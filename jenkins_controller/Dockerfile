FROM jenkins/jenkins:2.414.2-lts-jdk17
ENV JAVA_OPTS -Djenkins.install.runSetupWizard=false
COPY plugins.txt /usr/share/jenkins/ref/plugins.txt
USER root
RUN apt-get update && apt-get install -y python3 python3-pip
USER jenkins
RUN jenkins-plugin-cli -f /usr/share/jenkins/ref/plugins.txt