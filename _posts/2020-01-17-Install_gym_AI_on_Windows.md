---
layout: post
title: "Trick to install GymAI on Windows 10 and use it with Jupyter"
categories: [blog, engineering]
tags: [maths, engineering, reinforcement learning]
date: 2020-01-17
---



These are some hacks that allowed me to do two things:

1. Create a Python environment in Jupyter Notebooks

2. Install **gymAI** and use it with Notebooks

_____________________________________________________________________________________________________________________________________

# Create a Python environment using Anaconda GUI
This is the easiest way to create an environment. 

Click on *Environments* on the left side panel and follow the instructions. Make sure to select the python version you want.

<img src="https://lcipolina.github.io/images/2020-01-17/createEnv.PNG" width="600">

After the environment is created, you can see on that same tab, the packages installed.

After the new environment is created, go back to *Home* in the left side panel and switch from *Root* to the new environment created. This is how you change working environments.

<img src="https://lcipolina.github.io/images/2020-01-17/changeEnvs.PNG" width="600">

You will see the environment created and the applications and packages installed. IT also shows the location where the environment is created.

Now you will be able to work on Jupyter notebooks under this new environment.
_____________________________________________________________________________________________________________________________________

# Installing Jupyter Notebooks on the new environment
The easiest way is to install Jupyter using Anaconda GUI. After we have selected to work in the environment created, we will be given the option to install Jupyter as shown below.

<img src="https://lcipolina.github.io/images/2020-01-17/installJupy.PNG" width="600">

If everything goes well, we will have Jupyter installed and off we go.

There is a chance that Anaconda gives back an error and won't let us install Jupyter for whatever reason. Instead, Anaconda will ask us if we want to install Jupyter in another environment. Click *Yes*.

**Here is the trick:**

* We will install Jupyter in a new environment that Anaconda is creating for us. Let's call this environment *Notebook*

* You can either keep working on this *Notebook* environment, or you can clone it.

* To clone an environment, simply go to where you created a new environment and select *clone* on the bottom

* If you clone this *Notebook* environment, you will now have an environment named *gym* but with a usable Jupyter Notebooks on it.

* Note that to name the cloned environment *gym*, you will have to delete the previous gym env (the one that we couldn't install the notebook on it).

* After the *Notebook* environment is cloned into *gym* we are able to install new packages into this environment.

* Note: if you notices that Anaconda freezes, dont' worry, just close it after a while.

_____________________________________________________________________________________________________________________________________

# Installing gym on the new environment
Open a Conda Promt shell and type the following:

1. If you want you can update conda just in case (on the conda shell)

    >> conda update conda

2. First we will install the usual packages in our environment: Python, Pip, Kernel manipulations and Git

   >> conda install python=3.7.4 (or the version you want)
   
   >>  conda install pip
   
   >>  conda install nb_conda_kernels –y
   
   >>  pip install gitpython

**Notes:**  
If you have problems with the SSL, you can isntall it from here. Just download it and run the installer:

[https://slproweb.com/products/Win32OpenSSL.html](https://slproweb.com/products/Win32OpenSSL.html)

3. Now we can install the rest of gym packages

Pretty much follow the steps here, except for the GIT installation (where we did pip install gitpython)

[https://towardsdatascience.com/how-to-install-openai-gym-in-a-windows-environment-338969e24d30](https://towardsdatascience.com/how-to-install-openai-gym-in-a-windows-environment-338969e24d30)

_____________________________________________________________________________________________________________________________________

# Test the environment
We will follow the testing procedure described in the link above, but using Jupyter Notebooks:

1. Open Anaconda and select the environment we've just created (as shown in the picture above)

2. Click on *Launch* a new Jupyter Notebook

3. An instance of Jupyter will open inyour browser, now we need to tell it that we want a Notebook created in our new environment:

<img src="https://lcipolina.github.io/images/2020-01-17/newJupyter.PNG" width="700">

Now we can test our installation of *gym* using Jupyter Notebooks as explained above.

<img src="https://lcipolina.github.io/images/2020-01-17/test.PNG" width="700">

