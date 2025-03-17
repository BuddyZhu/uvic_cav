# ROS2 Basic
This document will introduce the basic concepts of ROS2 to help you quickly get started with ROS2 functionalities related to CAV applications.

The raw documentation can be found [here](https://docs.ros.org/en/foxy/index.html).

# 1 The Ubuntu System
If you are already familiar with terminal interactions in the Linux system, you can skip this section.

Users commonly interact with an operating system in two ways: through the GUI interface (also known as desktop operations) and command-line interaction. Essentially, both serve the same purpose—operating software by clicking certain areas or entering specific commands.

When using simulators or debugging real vehicles, we often need to interact directly with the command line. Therefore, understanding basic command-line operations is a prerequisite for further learning ROS2.

At CAV Club, our vehicles run on the Ubuntu 20.04 operating system, so you need to learn the relevant concepts and usage methods.

## 1.1 Basic commands

### 1.1.1 `ls`/`cd`/`pwd`
Use `ls` to see what is inside this directory.
```
$ ls
f1tenth     Desktop     Downloads       ...
```

Use `pwd` to see which directory you are in currently.
```
$ pwd
/home/f1tenth
```

Use `cd` to change your working directory.
```
$ cd f1tenth
$ pwd
/home/f1tenth/f1tenth
```

### 1.1.2 `source`
Source is one the commands to execute some commands in a file. You will need to use `source` to add ros2 to your system path. Path is the directory where the system will find the executable in. After installation, the ROS2 will be in the `/opt/ros/foxy`. If you do not add this directory to path, system will not be able to find the program.
```
$ ros2 -h
-bash: ros2: command not found
```

```
$ source /opt/ros/foxy/setup.bash 
$ ros2 -h
usage: ros2 [-h] Call `ros2 <command> -h` for more detailed usage. ...
```

### 1.1.3 `apt`
`apt` is the package manager for Ubuntu system. You can treat it like an App Store which can install the software you want to use.
```
apt install nano
[sudo] password for <username>: 
Reading package lists... Done
Building dependency tree       
Reading state information... Done
Suggested packages:
  hunspell
The following NEW packages will be installed:
  nano
0 upgraded, 1 newly installed, 0 to remove and 0 not upgraded.
```

### 1.1.4 `sudo`
Add sudo prior to your command if you meet permission fault.

```
$ apt install nano
E: Could not open lock file /var/lib/dpkg/lock-frontend - open (13: Permission denied)
E: Unable to acquire the dpkg frontend lock (/var/lib/dpkg/lock-frontend), are you root?
```
Add `sudo`
```
$ sudo apt install nano
[sudo] password for <username>: 
Reading package lists... Done
Building dependency tree       
Reading state information... Done
Suggested packages:
  hunspell
The following NEW packages will be installed:
  nano
0 upgraded, 1 newly installed, 0 to remove and 0 not upgraded.
```

## 1.2 Useful softwares
### 1.2.1 `cat`/`vim`
`cat` is a command to display a text file in the command line. `vim` is a command, as well as a program to edit text files in the command line. 
```
$ ls
Desktop    Downloads  Pictures	sim_ws	   text.txt     Documents  Music      Public	Templates  Videos
$ cat text.txt 
Hello world!
```
```
$ vim text.txt
```
```
Hello world!
~                                                                               
~                                                                               
~                                                                      
~                                                                               
~                                                                               
"text.txt" 1L, 13C                      1,12          All
```

When you are in the `vim`:

Press `i` for INSERT mode:

```
Hello world!

I love CAV Club.          
~                                                                               
~                                                                               
~                                                                               
--INSERT--                 3,17          All
```

Press `esc` to quit INSERT mode.

Press `:q` + `enter` to quit vim without saving.

Press `:wq` + `enter` to save and quit vim.

After using `wq`:
```
$ vim text.txt 
$ cat text.txt 
Hello world!

I love CAV Club.
```

# 2. ROS2
## 2.1 ROS2 concepts
### 2.1.1 [Node](https://docs.ros.org/en/foxy/Tutorials/Beginner-CLI-Tools/Understanding-ROS2-Nodes/Understanding-ROS2-Nodes.html)

### 2.1.2 [Topics](https://docs.ros.org/en/foxy/Tutorials/Beginner-CLI-Tools/Understanding-ROS2-Topics/Understanding-ROS2-Topics.html)

### 2.1.3 [Parameters](https://docs.ros.org/en/foxy/Tutorials/Beginner-CLI-Tools/Understanding-ROS2-Parameters/Understanding-ROS2-Parameters.html)

### 2.1.4 [Launch&nbsp;File](https://docs.ros.org/en/foxy/Tutorials/Beginner-CLI-Tools/Launching-Multiple-Nodes/Launching-Multiple-Nodes.html)

## 2.2 ROS2 coding
