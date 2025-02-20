# Ashton Majachani
Cybersec portfolio  
Feb 20th 2025

# Authentication + Authorization in Linux

## Project description

In this lab, I need to gain hands-on experience on how to add users and manage user access in a system. These skills can be used when working with authentication technology. I will use useradd, usermod, userdel, and chown commands to manage user access in the Linux Bash shell, prefixing these commands with sudo.

## Add a new employee
I need to add a user called researcher9 to the system. They must be added to the research_team group. I used the usermod command and -g option to add researcher9 to the research_team group as their primary group.

The following code demonstrates how I used Linux commands to add a new employee in the file system: 
# sudo useradd researcher9
# sudo usermod -g reearch_team researcher9


## Change ownership of a file
The new employee, researcher9, will take responsibility for project_r. In this task, I am to make them the owner of the project_r.txt file. The project_r.txt file is located in the /home/researcher2/projects directory, and owned by the researcher2 user. Using the chown command, I want to make researcher9 the owner of /home/researcher2/projects/project_r.txt.

# cd /home/researcher2/projects
# sudo chown researcher9 project_r.txt


## Add the new employee to a new group

A couple of months later, this employee's role at the organization has changed, and they are working in both the Research and the Sales departments. I want to add researcher9 to a secondary group (sales_team). Their primary group is still research_team.
Using the usermod command with the -a and -G options to add researcher9 to the sales_team group as a secondary group:
# sudo usermod -a -G sales_team researcher9


## Delete the employee from the system

A year later, researcher9, decided to leave the company. I must remove them from the system:
# sudo userdel researcher9
then i run the following, since thet were created as the only user in the group:
#sudo groupdel researcher9

## Summary

I gained hands on experienced using bash commands to add a new user, add the user to a group, change user permissions on files and delete user from the system.