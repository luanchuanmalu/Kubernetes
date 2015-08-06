# mongod process on latest CentOS
# See https://docs.docker.com/articles/dockerfile_best-practices/
 
FROM centos                             # Base container on latest CentOS release
MAINTAINER Yang <yang@mongodb.com>
 
COPY mongodb.repo /etc/yum.repos.d/     # Copy yum repo config file to add MongoDB repo
RUN yum install -y mongodb-org-server   # Install mongod
RUN mkdir -p /data/db                   # Create default dbpath
 
ENTRYPOINT [ "mongod" ]                 # Execute the mongod binary on container startup