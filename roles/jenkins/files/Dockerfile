FROM jenkins/jenkins:lts

USER root

RUN apt-get update && \
    apt-get install -y python3 python3-pip sudo && \
    pip3 install ansible --break-system-packages && \
    apt-get clean

USER jenkins
