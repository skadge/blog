MORSE 1.0 is out!
=================

.. image:: https://raw.github.com/laas/morse/master/doc/media/morse-logo.png
  :align: center
  :height: 192

Just to briefly mention that, after 4 years of world-wide development,
MORSE-1.0 is finally out!

What comes with MORSE?
----------------------

* Versatile 3D simulator for mobile robots simulation (single or multi robots),

* Realistic ('modern' OpenGL) and dynamic environments (interaction with other
  agents like humans or objects),

* Based on well known and widely adopted open source projects (Blender for
  real-time 3D rendering, Bullet for physics simulation, dedicated robotic
  middlewares for communications),

* Command-line oriented (with optional scene editing in Blender), entirely
  scriptable in Python,

* Adaptable to various level of simulation abstraction (e.g. simulate cameras
  as video-streams, depth-streams or semantic maps depending on your needs),

* > 20 classes of sensors (including depth sensors, cameras, IMU, laser
  scanners...), > 15 classes of actuators (including kinematic chains,
  quadrirotor control, force control...) are available. Detailed documentation
  explain how to add new ones (in C or Python),

* Currently supports ROS, YARP, MOOS and Pocolibs + direct socket interface

* `Extensive documentation <http://www.openrobots.org/morse/doc/stable/morse.html>`_


.. image:: https://raw.github.com/laas/morse/master/doc/media/outdoors.png
  :align: center
  :height: 400

You can `get the code on GitHub <http://github.com/laas/morse>`_.
