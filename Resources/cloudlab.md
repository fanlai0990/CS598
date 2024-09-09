# Using CloudLab

In this course, You can use CloudLab resources for your project.
CloudLab is a research facility which provides bare-metal access and control over a substantial set of computing, storage, and networking resources. 
If you haven't worked in CloudLab before, you need to [register a CloudLab account](https://cloudlab.us/signup.php).

This document walks you through the CloudLab registration process and shows you how to start an experiment in CloudLab. 

*Most importantly, it introduces our policies on using CloudLab that will be enforced throughout the semester.*

## Register A CloudLab Account

To register an account, please use your UIUC email account and NetID. 
Upload your SSH public Key file as you will be using SSH to access the nodes CloudLab assigns to you. 
Click on `Join Existing Project` and enter `UIUC-AISys` as the project name. 
Then click on `Submit Request`. 
The project leader (Prof. Lai) will approve your request. 
See the screenshot below. 
![Screenshot-Register](https://github.com/user-attachments/assets/8ca448d0-a371-4d7f-b299-4f90f933a5b0)

If you already have a CloudLab account, simply request to join the `UIUC-AISys` project.

## Start An Experiment
To start a new experiment, go to your CloudLab dashboard and click on the `Experiments` tab in the upper left corner, then select `Start Experiment`. 
This will lead to the profile selection panel. 
Click on `Change Profile`, and select a profile from the list. 
Select the profile and click on `Next` to move to the next panel. 
Here you should name your experiment with `<NetID>-A1`. The purpose of doing this is to prevent everyone from picking random names and ending up confusing each other since everyone in the `UIUC-AISys` project can see a full list of experiments created.
You also need to specify from which cluster you want to start your experiment. Each cluster has a variety of hardware. For more information on the hardware CloudLab provides, please refer to this [page](http://docs.cloudlab.us/hardware.html).

![Screenshot-SelectCluster](https://github.com/user-attachments/assets/3ca21039-6b79-4e7e-8b3d-4ddaf002bd4b)

## Reserving Hardware
To ensure the availability of your cluster, we recommend that you apply for a reservation first. Nodes can be reserved at `My Experiments > Reserve Nodes`. To increase the likelihood of your reservation being approved, we recommend selecting [hardware types](http://docs.cloudlab.us/hardware.html) with many nodes, e.g., 3 m510 nodes at CloundLab Utah. Note that some hardware types have ARM or POWER architecture processors, which might not have supported PyTorch builds.

![Screenshot-ReserveNodes](https://github.com/user-attachments/assets/4904882f-1aa3-41ad-aa28-52152d8c0c42)

## Policies on Using CloudLab Resources
1. The nodes you receive from CloudLab are real hardware machines sitting in different clusters. Therefore, we ask you not to hold the nodes for too long. CloudLab gives users 16 hours to start with, and users can extend it for a longer time. Manage your time efficiently and only hold onto those nodes when you are working on the assignment. You should use a private git repository to manage your code, and you must terminate the nodes when you are not using them. If you do have a need to extend the nodes, do not extend them by more than 1 day. **We will terminate any cluster running for more than 48 hours.**
2. As a member of the `UIUC-AISys` project, you have permissions to access another member's private user space. **Stick to your own space and do not access others' to peek at/copy/use their code, or intentionally/unintentionally overwriting files in others' workspaces.** For more information related to this, please refer to the [UIUC Sieber School Honor Code](https://siebelschool.illinois.edu/academics/honor-code). 
