FROM openease/kinetic-swi
MAINTAINER Daniel Beßler, danielb@cs.uni-bremen.de

# Initialize the catkin workspace
USER ros
WORKDIR /home/ros/src
RUN /usr/bin/python /opt/ros/kinetic/bin/catkin_init_workspace

RUN echo "Adding repositories...."
ADD ./src.tar /home/ros/src/
USER root
RUN chown -R ros:ros /home/ros/src/
USER ros

WORKDIR /home/ros
# Build the catkin workspace
RUN /opt/ros/kinetic/bin/catkin_make
# RUN /bin/bash
