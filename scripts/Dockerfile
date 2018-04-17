FROM jenkins/jenkins:lts
# if we want to install via apt
USER root
RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install sudo -y
RUN adduser jenkins sudo
RUN sed -i -e 's/Defaults    requiretty.*/ #Defaults    requiretty/g' /etc/sudoers
USER jenkins
