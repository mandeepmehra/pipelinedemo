FROM jenkins:2.60.3-alpine

USER jenkins
RUN mkdir -p /var/jenkins_home/jobs/pet-clinic-job

USER jenkins
COPY config.xml /var/jenkins_home/jobs/pet-clinic-job/config.xml

COPY plugins.txt /usr/share/jenkins/ref/plugins.txt
RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/ref/plugins.txt

