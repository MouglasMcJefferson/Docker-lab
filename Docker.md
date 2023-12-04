# Docker Lab-OpenVAS
Here is the link which I used to follow and open openvas on docker in ubuntu 

- https://www.youtube.com/watch?v=jgVt4QgvtRc&ab_channel=ITBestPractice
## Installing Docker
First we install docker on our system

    sudo apt install docker.io

Then we update and install plugins

    sudo apt update
    sudo apt install docker-compose
Don't forget to upgrade 
   
    sudo apt upgrade
Next check to see if docker is running
    
    sudo docker docker status
if it is not running use this and check again

    sudo service docker start
## installing docker container
The container that I used was this one

    sudo docker run -d -p 443:443 --name openvas mikesplain/openvas

https://github.com/mikesplain/openvas-docker
## Using openvas for target scan
For using openvas i went to 8:00 and followed this tutorial for assistance in navigating

https://www.youtube.com/watch?v=lReXcE9BT0g&ab_channel=CyberOffense

1. Next we go into our webbrowser and go to 
2. https//:localhost/
3. Password and username are admin
4. Head to configure and select targets
5. Create your target to scan. I scanned google at 8.8.4.4
6. Next go to scans and task, once there either directly scan an ip or create a task to scan a target
7. Once task is created run the task ( i named mine scan google) and then wait as it will take a while
8. After your task(s)are done head to scnas and view your results
