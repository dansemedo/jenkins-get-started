## Getting started with Jenkins

##### Run your Jenkins container and give backup abilities mapping the configuration files in your Linux VM (outside the container), this will help you to update Jenkins just downloading a new release.
docker run -p 80:80 -p 443:443 -p 8080:8080 -p 50000:50000 -v jenkins_home:/var/jenkins_home jenkins/jenkins:lts

##### Give auto healing (auto-restart) abilities to your Jenkins container:
docker run -dit --restart unless-stopped jenkins

##### Get access to the container and install dotnet core and other things (you can create a Dockerfile that install everything that you need)
sudo docker exec -it <mycontainer> bash

##### RMATE - very useful to edit files and scripts in Linux, works pretty well with VSCODE:
https://medium.com/@prtdomingo/editing-files-in-your-linux-virtual-machine-made-a-lot-easier-with-remote-vscode-6bb98d0639a4
##### Access to the Linux VM with RMATE 
ssh -R 52698:localhost:52698 <user@vmnameDNS>
