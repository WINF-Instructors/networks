FROM debian:latest

RUN apt update && apt install  openssh-server -y

RUN useradd -r -m -d /home/ubuntu -s /bin/bash -g root -u 1000 test 

RUN echo 'test:test' | chpasswd

RUN service ssh start

CMD ["/usr/sbin/sshd", "-D"]
