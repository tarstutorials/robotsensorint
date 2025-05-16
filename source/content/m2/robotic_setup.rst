===================================================
Getting Started with Kinova
===================================================

In these tutorials we will be using the Kinova 7DoF Gen3 Robotic arm. If you are using a Kinova arm, this part of the tutorial will be beneficial to set up the basics of connecting to the robot and downloading the Kinova Kortex API.
If you would like to lean more about the Kinova Gen 3, you can head to their `website <https://www.kinovarobotics.com/product/gen3-robots>`_.

.. note::
    For this tutorial, the authors use the python version of the Kinova Kortex Api. For C++ users, please refer to the quick start `guide <https://github.com/Kinovarobotics/Kinova-kortex2_Gen3_G3L?tab=readme-ov-file#quick-start-for-c-users>`_.

------------------------
Connecting to the Robot
------------------------

Kinova provides a great `quick start guide <https://drive.google.com/file/d/1vZHA3fQS3-5kkncsnYLjH8qAFj4wS6PJ/view>`_ that covers everything you need to know to configure your computer and establish a connection with the robot.
If you never have used a Kinova Robot, this guide will help you setup your network and robot.

---------------------------------------------------------
Downloading Kinova Kortex API
---------------------------------------------------------

For this tutorial we will be using Python 3.8.10 and Kortex Kortex Python API.
If you don't have Python 3.8.10 installed, please refer to the `Python website <https://www.python.org/downloads/release/python-3810/>`_.

To begin, download the API .whl file using this `link <https://artifactory.kinovaapps.com/ui/native/generic-public/kortex/API/2.6.0/kortex_api-2.6.0.post3-py3-none-any.whl>`_.

---------------------------
Creating a Project Folder
---------------------------

For these tutorials, we will setup a single project folder to organize all your scripts and example code.
I'll be using Visual Studio Code, but you're welcome to use any editor you prefer.

Here are the steps to create your project folder and get started: 

#. Open your terminal

#. Create a new folder for your project

    .. code-block:: python

        mkdir RobotSensorIntegration
        cd RobotSensorIntegration

#. Open the folder in Visual Studio Code  
    
    .. code-block:: python
        
        code .

This will open your project in vs Code.
From here we will create a virtual environment to manage python packages. Since this project will involve several pip installations, using a virual environment will help prevent conflicts with other projects.

#. Start by being inside your project folder (RobotSensorIntegration)

#. In your terminal write:

    .. code-block:: python

        python -m venv myenv
    
    This creates a virtual environment named myenv using Python 3.8.10
#. Activate your environment using:

   .. code-block:: python

       .\myenv\Scripts\activate

Now that we have the virtual environment setup, you will want to install the .whl file.
Here is the code to install that:

.. code-block:: python

    python -m pip install <whl fullpath name>.whl

Now that we have the API installed, we can download the examples.
The three examples that are important are API creation, gripper commands, and cartesian waypoint trajectories.
You will eventually combine all of these into a single script when we bring in the sensor data, so its a good idea to understand how each one works on its own first.
For now, copy these example scripts into your RobotSensorIntegration folder:

.. include:: C:\Users\avame\Desktop\CVPRDemo\Python\01-api_creation.py
    :code: python

.. include:: C:\Users\avame\Desktop\CVPRDemo\Python\01-gripper_command.py
    :code: python

.. include:: C:\Users\avame\Desktop\CVPRDemo\Python\02-send_cartesian_waypoint_trajectory.py
    :code: python