===================================================
Data Collection with Physiological Sensors
===================================================

In this section, we explore how to collect data using physiological sensors, specifically Surface Electromyography (sEMGs) sensors to communicate with the robot.
We will be using the Delsys Trigno Avanti system in this tutorial. We do not go over an introduction of these sensors in this tutorial, but we have in our VR `tutorials <https://tarstutorials.github.io/vrsensorint/content/m3/intro_to_sensors.html>`_. If you're unfamiliar with these types of sensors, we highly recommend reviewing that first.

-------------------------------
Delsys API
-------------------------------

We use the Delsys `Trigno Avanti <https://delsys.com/trigno-avanti/>`_, which is the "standard" sEMG sensor used in our setup.
There are twoways you can use the sensors, 
#. The Delsys Software: Trigno Discover
    This is the main option for using the sensor, which provides a user-friendly GUI for the sensors and a way to collect the data.
    .. note::
        We won't be using this option in this tutorial, but if you would like to learn more about this option, we cover setup instructions in our `VR tutorial <https://tarstutorials.github.io/vrsensorint/content/m4/data_collection.html>`_.

#. The Delsys API
    We will be using the Delsys API, which allows you to communicate with your Trigno System and sensors. This will allow you to get all of the data which your sensors read and output it the way you want in Python.

----------------------------
Setting up the API
----------------------------

To get stated with the Delsys API, we have to clone it from the Delsys `github <https://github.com/delsys-inc/Example-Applications>`_ and install the necessary dependencies.

Heres how to do that:

    #. Open your project in vscode or your preferred editor
    
    #. Open the terminal and paste:
        
        .. code-block:: python

            git clone https://github.com/delsys-inc/Example-Applications.git


Once the repository is cloned, you will see a folder named **Example-Applications** in your project directory.
This folder will have a python folder inside which is what we will be focusing on.

You will want to change directories into Example-Applications and the Python directory with

.. code-block:: python

    cd Example-Applications/Python

Once you are in the Python directory, you will want to install the required dependencies using:

.. code-block:: python

    pip install -r requirements.txt

Once this is installed, you should copy and paste your key/license strings that was provided to you by Delsys Inc. in /AeroPy/TrignoBase.py.

If you plug in your Trigno base station you can run the demo with:

.. code-block:: python

    python DelsysPythonDemo.py

This demo shows live data being collected from your sensors. Feel free to explore and modify it to get a better sense of how the system works. If you have questions about them feel free to contact the authors.