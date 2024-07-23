FROM ubuntu:latest

# Install necessary packages
RUN apt-get update && \
    apt-get install -y software-properties-common sudo \
    && apt-get install -y iputils-ping \
    && apt-get install -y openssh-server  \
    && service ssh start \
    && apt-get clean
# Expose port 22 (for SSH, if necessary)
EXPOSE 22