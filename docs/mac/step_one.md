+++
title = "Install Docker on OS X"
description = "Getting started with Docker"
keywords = ["install, demo, Docker, OS X"]
[menu.mac]
identifier = "mac_install"
weight = 1
+++

# Install Docker Mac OS X

You install Docker using Docker Toolbox. Docker Toolbox includes the following Docker tools:

* Docker Machine for running the `docker-machine` binary
* Docker Engine for running the `docker` binary
* Docker Compose for running the `docker-compose` binary
* Kitematic, the Docker GUI
* a shell preconfigured for a Docker command-line environment
* Oracle VM VirtualBox 

Because the Docker daemon uses Linux-specific kernel features, you can't run
Docker natively in OS X. Instead, you must use `docker-machine` to create and
attach to a Docker VM on your machine. This VM hosts Docker for you on your Mac.

## Step 1: Check your version

Your Mac must be running OS X 10.6 "Snow Leopard" or newer to run Docker.
To find out what version of the OS you have:

1. Choose **About this Mac** from the Apple menu. 

    ![Which version](/mac/images/which_version.png)

    The version number appears directly below the words `OS X`.

2. If you have the correct version, go to the next step.

    If you aren't using a supported version, you could consider upgrading your
    operating system.


## Step 2: Install Docker Toolbox

1. Go to the <a href="https://www.docker.com/toolbox" targe="_blank">Docker Toolbox</a>.

2. Click the installer link to download.

3. Install Docker Toolbox by double-clicking the package or by right-clicking
and choosing "Open" from the pop-up menu.

    The installer launches the "Install Docker Toolbox" dialog.
    
    ![Install Docker Toolbox](/mac/images/mac-welcome-page.png)

4. Press **Continue** to install the toolbox.

    The installer presents you with options to customize the standard
    installation. 
  
    ![Standard install](/mac/images/mac-page-two.png)
  
    By default, the standard Docker Toolbox installation:
  
    * installs binaries for the Docker tools in `/usr/local/bin` 
    * makes these binaries available to all users 
    * updates any existing Virtual Box installation 
  
    For now, don't change any of the defaults.

5. Press **Install** to perform the standard installation.

     The system prompts you for your password.
   
     ![Password prompt](/mac/images/mac-password-prompt.png)
   
6. Provide your password to continue with the installation.

     When it completes, the installer provides you with some information you can
     use to complete some common tasks. You can ignore these for now.
   
     ![All finished](/mac/images/mac-page-finished.png)
   
7. Press **Close** to exit.



## Step 4. Verify your installation

To run a Docker container, you:

* create a new (or start an existing) Docker virtual machine 
* switch your environment to your new VM
* use the `docker` client to create, load, and manage containers

Once you create a machine, you can reuse it as often as you like. Like any
Virtual Box VM, it maintains its configuration between uses.

1. Open the **Launchpad** and locate the Docker Quickstart Terminal icon.

    ![Launchpad](/mac/images/applications_folder.png)
    
2. Click the icon to launch a Docker Quickstart Terminal window.

    The terminal does a number of things to set up Docker Quickstart Terminal for you. 
    
        Last login: Sat Jul 11 20:09:45 on ttys002
        bash '/Applications/Docker Quickstart Terminal.app/Contents/Resources/Scripts/start.sh'
        Get http:///var/run/docker.sock/v1.19/images/json?all=1&filters=%7B%22dangling%22%3A%5B%22true%22%5D%7D: dial unix /var/run/docker.sock: no such file or directory. Are you trying to connect to a TLS-enabled daemon without TLS?
        Get http:///var/run/docker.sock/v1.19/images/json?all=1: dial unix /var/run/docker.sock: no such file or directory. Are you trying to connect to a TLS-enabled daemon without TLS?
        -bash: lolcat: command not found

        mary at meepers in ~
        $ bash '/Applications/Docker Quickstart Terminal.app/Contents/Resources/Scripts/start.sh'
        Creating Machine dev...
        Creating VirtualBox VM...
        Creating SSH key...
        Starting VirtualBox VM...
        Starting VM...
        To see how to connect Docker to this machine, run: docker-machine env dev
        Starting machine dev...
        Setting environment variables for machine dev...

                                ##         .
                          ## ## ##        ==
                       ## ## ## ## ##    ===
                   /"""""""""""""""""\___/ ===
              ~~~ {~~ ~~~~ ~~~ ~~~~ ~~~ ~ /  ===- ~~~
                   \______ o           __/
                     \    \         __/
                      \____\_______/

        The Docker Quick Start Terminal is configured to use Docker with the “default” VM.

3.  Click your mouse in the terminal window to make it active.

    If you aren't familiar with a terminal window, here are some quick tips. 
    
    ![Teriminal](/tutimg/terminal.png) 
    
    The prompt is traditionally a `$` dollar sign. You type commands into the
    *command line* which is the area after the prompt. Your cursor is indicated
    by a highlighted area or a `|` that appears in the command line. After
    typing a command, always press RETURN.

4. Type the `docker run hello-world` command and press RETURN.

    The command does some work for you, if everything runs well, the command's
    output looks like this:
    
        $ docker run hello-world
        Unable to find image 'hello-world:latest' locally
        Pulling repository hello-world
        91c95931e552: Download complete 
        a8219747be10: Download complete 
        Status: Downloaded newer image for hello-world:latest
        Hello from Docker.
        This message shows that your installation appears to be working correctly.

        To generate this message, Docker took the following steps:
         1. The Docker client contacted the Docker daemon.
         2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
            (Assuming it was not already locally available.)
         3. The Docker daemon created a new container from that image which runs the
            executable that produces the output you are currently reading.
         4. The Docker daemon streamed that output to the Docker client, which sent it
            to your terminal.

        To try something more ambitious, you can run an Ubuntu container with:
         $ docker run -it ubuntu bash

        For more examples and ideas, visit:
         https://docs.docker.com/userguide/


## Where to go next

At this point, you have successfully installed Docker. Leave the Docker Quickstart Terminal
window open. Now, go to the next page to [read a very short introduction Docker
images and containers](/mac/step_two).


&nbsp;