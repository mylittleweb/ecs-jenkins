FROM jenkins/jenkins:2.249.1-jdk11

ENV JAVA_OPTS -Djenkins.install.runSetupWizard=false

COPY usr/share/jenkins/ref /usr/share/jenkins/ref/

RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/ref/plugins.txt
