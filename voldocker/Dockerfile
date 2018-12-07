

FROM centos:7

# Setup user environment
RUN useradd -d /home/saluser -m saluser

# Create a shared data volume
RUN mkdir /var/shared/
RUN chown -R saluser:saluser /var/shared
VOLUME /var/shared

WORKDIR /home/saluser

# Link in shared parts to the home directory
RUN ln -s /var/shared /home/saluser/shared

RUN mkdir /home/saluser/develop
RUN chmod 777 /home/saluser/develop

RUN chown -R saluser: /home/saluser
USER saluser

CMD /bin/bash
