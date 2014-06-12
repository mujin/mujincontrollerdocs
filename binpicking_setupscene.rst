Scene Editing
=============

Copy Robot to New Scene
-----------------------

All robots should be in COLLADA format (*.mujin.dae). When creating a new scene, first copy the robot into its own scene. For example, call the scene **binpickingtutorial**

Importing CAD models to scene
-----------------------------

1. First setup a network drive that allows CAD models to be uploaded to the Mujin Controller filesystem. :ref:`file_upload`

2. Upload the CAD model.

3. On the scenes list page, click on "Import to COLLADA scene" and select the CAD model. Now the CAD model should be converted to COLLADA (*.mujin.dae)

4. On the **binpickingtutorial** scene page, add a new instance object by clicking on "+Add Object".

  - Select the newly converted COLLADA file.
  - Reposition the part using the WebGL window or inputting the text.
  - Press the "Save" button when done.

Editing Objects
---------------

Each instance object has a translation, orientation, and DOF values (joint values). Robots also have a way to "grab" other instance objects like tools.

WebGL controls are located on the lower left of the WebGL window: one is for moving the camera, the other is for moving objects. Press the "Save" button when done.

Grabbing
++++++++

A instance object can be permenantly attached to any robot link so that whenever the robot moves, the botton follows.
In order for the robot to grab a instance object, select the robot and click the "Grabs" tab. Add Grab and select the instance object to grab and the robot link to grab it with. In order to test that it works, go on "DOF Values" tab and move the robot around, the grabbed instance object should follow.

Initializing Bin with Parts
---------------------------

It is possible to initialize a bin with a bunch of parts using physics simulation.

1. On the **binpickingtutorial** scene page, click on **Binpicking Tasks** and create a new task.

2. On the right, click on the "Initialize Bin" tab, then

  1. Select the part CAD filename,
  2. Edit the number of parts to drop,
  3. Select container name to drop them in,
  4. Set the simulation time for dropping them
  5. Set a base name that each new target will be named with. For exampling setting "target_" will product new instance objects with names "target_0", "target_1", etc.
  6. Click on "Start simulation" to start. When the simulation time passes, simulation will automatically stop. Or can force stop using "Stop simulation" button.

3. Click on "Take snapshot" to permanently save the scene to a new COLLADA file. If this is not clicked, the current dynamic state will be lost when the Mujin Controller is restarted.

