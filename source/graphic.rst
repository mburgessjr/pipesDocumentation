Object Map
=================================

|

.. image:: diagram.*

|

:ref:`PyNetwork` is a main class constructed around a :ref:`Network` that is meant to describe the whole network of pipes. It is held in :ref:`allthethings.pyx` as all main classes are

:ref:`Network` is a class that holds many :ref:`PyPipe_ps` objects together, representing the network of :ref:`Channels <Channel>`. It is held in :ref:`network.cpp`

:ref:`PyPipe_ps` is a main class constructed around a :ref:`Channel` object, describing a single pipe. Defined in :ref:`allthethings.pyx` as all main classes are

:ref:`Channel` is a class meant to describe the channel of a pipe or the pipe itself. It is tied to :ref:`Junction1`, :ref:`Junction2`, and :ref:`Junction3` objects and is constructed about a :ref:`Cpreiss` or :ref:`Cuniform` object. The class is defined in :ref:`channel.cpp`

:ref:`Cpreiss` is a class outlining a pipe that has a Preissman slot, meaning the edges are non-uniform. It is defined in :ref:`channel.cpp`

:ref:`Cuniform`	 is a class outlining a pipe that doesn't have a Preissman slot, meaning the edges are uniform. It is defined in :ref:`channel.cpp`

:ref:`Junction1` is a class that describes the junction of a single pipe. It is tied to a :ref:`Channel` object and defined in :ref:`channel.cpp`

:ref:`Junction2` is a class that describes the union of two pipes. It is tied to two :ref:`Channel` objects and defined in :ref:`channel.cpp`

:ref:`Junction3` is a class that describes the union of three pipes. It is tied to three :ref:`Channel` objects and it actually just a collection of three :ref:`Junction2` objects. It is defined in :ref:`channel.cpp`

:ref:`PyMystery_BC` is a main class required to determine the mysterious boundary conditions of a pipe. It is constructed around an :ref:`PyBC_opt_dh` object and uses a Levmar approximation at its base to determine the exterior conditions of the pipe. The class is defined in :ref:`allthethings.pyx`

:ref:`PyBC_opt_dh` is a class meant to approximate the mysterious relationships that exist a pipes boundary and optimize the change in pressure head over spacial increments. It is built around a :ref:`bc_opt_dh_c` object and is defined in :ref:`allthethings.pyx`

:ref:`bc_opt_dh_c` is a class that determines the mysterious boundary condiions of a pipe via a :ref:`Levmar` object. The class is defined in :ref:`optimizeit.cpp`

:ref:`Levmar` is class that allows the performing of a Levenberg-Marguardt optimization. This can be used to calculate how the mysterious boundary conditions of a pipe work, defined in :ref:`levmar.cpp`






	