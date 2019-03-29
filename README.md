# SSHD server on CentOS

**Docker Image with SSHD.**

The build of this project you can download as:

`` docker pull toolstodevops/centos-sshd:latest ``

For use, see the steps:

`` docker run -d -p <Local_port>:22 toolstodeveops/centos-sshd:latest ``

``ssh root@localhost/ip_docker -p <local_port>``

For change root password:

`` FROM kuramoto/centos-sshd:latest ``

``RUN echo root:<new_password> | chpasswd``

``EXPOSE 22``

``CMD ["/usr/sbin/sshd", "-D"]``
