FROM jenkins/jenkins:latest
USER root
RUN apt-get update \
  && apt-get install -y sudo \
  && apt-get install -y libltdl7 \
  && rm -rf /var/lib/apt/lists/*
RUN echo "jenkins ALL=NOPASSWD: ALL" >> /etc/sudoers
RUN groupadd docker
RUN usermod -aG docker jenkins
USER jenkins

