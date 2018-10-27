.. Aerial Robotics with ROS documentation master file, created by
   sphinx-quickstart on Mon Oct 22 17:18:54 2018.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Aerial Robotics Quick Start Guide
====================================================

.. note::
   Development of this guide is supported by `Dr. Girish Chowdhary <https://abe.illinois.edu/directory/girishc>`_ and members of his `Distributed Autonomous Systems Lab (DASLAB) <http://daslab.illinois.edu/>`_ at `UIUC <https://illinois.edu/>`_ and is primarily meant for its users. This guide is released under highly permissive MIT license which also makes it clear that the author and the research group he is a part of cannot be held liable to any damage caused by usage of this guide or any topic discussed in it. For a detailed statement, go through the `license file <https://pranay.mit-license.org/>`_.

This document is designed to get users started with testing nano quadcopters in the vicon motion capture arena using `Robotic Operating System (ROS) <http://www.ros.org/>`_ framework. The focus in on deploying and testing different control algorithms on an open source and open hardware nano quadcopter called `Crazyflie <https://www.bitcraze.io/crazyflie-2/>`_ and a closed hardware Simulink compatible nano drone called `Parrot Mambo <https://www.parrot.com/us/drones/parrot-mambo-fly/>`_.

The content of this guide is organized as follows:

* In the first section, we setup and learn about the necessary hardware including quadcopters, multiple computers which run off-board control algorithms, ROS nodes, mission planners, etc. and motion capture system to obtain accurate position and orientation information required for testing control algorithms. We also install and setup ROS and a few other tools that come in handy while working with ROS and Crazyflie.

* The second section is a primer to ROS. It details what ROS is (and importantly what ROS is not) and why one should work with ROS as the middleware for robotics development. We will cover the basic concepts of ROS with appropriate examples which include working with Crazyflie and then get into advanced concepts in ROS. We would also cover ROS interface with `Gazebo <http://gazebosim.org/>`_, a widely used robotics simulator.

* The third section discusses simulation environments for Crazyflie and Mambo in Gazebo and Simulink. We also detail the process of accessing real-time vicon data in ROS and MATLAB environment.

* In the final section, we deploy and test different control algorithms on Crazyflie. This section describes both on-board controllers and off-board controllers which communicate with Crazyflie through ROS. This is the part where we get our hands dirty as this involves tinkering with the firmware and working with the hardware to tune our controllers.

Any user of this guide is expected to have working knowledge of python (and preferably C/C++). The third section involves simulink models which requires basic knowledge of `MATLAB <https://in.mathworks.com/products/matlab.html>`_ and `Simulink <https://in.mathworks.com/products/simulink.html>`_. Finally, basic understanding of flight dynamics and co-ordinate transformations would help in debugging any issues with the code.

.. danger::
   * Flying unmanned aerial systems outdoors is regulated by the `FAA <https://www.faa.gov/>`_ in United States and by similar agencies in most of the other countries. Ensure that you follow all the `regulations <https://www.faa.gov/uas/>`_ and have the required license/permission to fly.
   * Flying indoors can pose several risks to people, equipment and could also be a fire hazard. Ensure that you fly in an assigned closed area and go through this useful `document <https://drones.princeton.edu/sites/drones/files/indoor_safety_guidelines.pdf>`_ on indoor flight safety.

.. toctree::
   :maxdepth: 2
   :caption: Hardware and Environment Setup

   one/mocapsystem
   one/env-setup
   one/quad-setup


.. toctree::
   :maxdepth: 2
   :caption: ROS Quick Guide

   two/intro-ros
   two/nodes-topics.rst
   two/pub-sub.rst
   two/services.rst
   two/rviz-rqt.rst
   two/gazebo.rst

.. toctree::
   :maxdepth: 2
   :caption: Simulation and Data Streaming Tools

   three/simulink-models
   three/ros-streaming
   three/matlab-streaming

.. toctree::
   :maxdepth: 2
   :caption: Control Algorithms Development

   four/control-devel

.. toctree::
   :maxdepth: 2
   :caption: Miscellaneous

   five/faatest-prep
