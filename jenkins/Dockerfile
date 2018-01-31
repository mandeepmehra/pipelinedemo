FROM jenkins:2.60.3-alpine
MAINTAINER "Mandeep Mehra"

USER jenkins

COPY --chown=jenkins:jenkins config.xml /var/jenkins_home/jobs/pet-clinic-job/config.xml
COPY --chown=jenkins:jenkins petclinic /var/jenkins_home/petclinic 

WORKDIR /var/jenkins_home/petclinic
RUN git config --global user.name "Mandeep Mehra" && git config --global user.email "mmehra@xebialabs.com" && git init && git add . && git commit -m "Initial Commit" 

COPY plugins.txt /usr/share/jenkins/ref/plugins.txt
RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/ref/plugins.txt
