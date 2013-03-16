HOAP3 loves to write letters
============================

HOAP3 is a sweet little humanoid robot build by Fujitsu, that first appeared on
the market in 2005 (and has already retired since a couple of years, actually).

.. image:: http://shyrobotics.com/wp-content/uploads/2012/02/hoap3_1.jpg
  :align: center
  :height: 300

In the *CoWriter* project, we want to have a robot helping children to acquire
writing skills, and so we need to get the HOAP3 robot to write on a piece of
paper.

I've decided to take this opportunity to test a very recent project from the
ROS galaxy: `MoveIt! <http://moveit.ros.org>`_.

Let see how to set together all the pieces to get our HOAP3 to its first
written words.

Building the robot's model
--------------------------

To use the ROS tools, you first need a ROS-compatible robot model, *ie*, a URDF
description of the robot.

I knew that HOAP3 was avaiable in the `LASA <http://lasa.epfl.ch>`_'s
`RobotToolKit <http://lasa.epfl.ch/RobotToolKit/>`_ simulator. After getting
the source, I quickly discovered that RobotToolKit models were built from an
custom XML description and a set of OBJ meshes.

After a bit of Python magic, and quite a lot of burned neurons to get the right
rotation matrices, I was able to generate `URDF files from RobotToolKit
descriptions
<https://github.com/severin-lemaignan/hoap3_description/blob/master/tools/to_urdf.py>`_
(thanks to the invaluable help of Christoph Gohlke `transformations.py`
library), and `Collada files from OBJ
<https://github.com/severin-lemaignan/hoap3_description/blob/master/tools/obj2dae.py>`_
(light adaptation from an existing batch conversion script using Blender.
Attention, requires Blender 2.66 for correct OBJ importation!)

You can get the resulting URDF file here, as a ROS package: `hoap3_description
<https://github.com/severin-lemaignan/hoap3_description>`_.

And the resulting model, viewed in RViz with this command:

.. code-block:: shell

  roslaunch hoap3_description display.launch

.. image:: |filename|/images/rviz_hoap3.png
  :align: center
  :height: 300


Preparing for motion planning
-----------------------------

.. raw:: html

    <video width="720" height="576" controls>
        <source src="|filename|/videos/hoap3_writing.mp4" type="video/mp4">
        <source src="|filename|/videos/hoap3_writing.ogv" type="video/ogg">
        Your browser does not support the video tag: you won't see HOAP3 writing :'-(
    </video>

*...to be continued!*


