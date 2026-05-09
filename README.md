# nodejs-app-deploy

nodejs-app-deploy by Github-Action

step:1

1) create folder in local and open that open in VS code terminalinstall npm `sudo apt install npm` then npm inilization `npm init`
     
-
2) install dependices like express `npm i express` then dev-dependices `npm i @types/express -D`

-
3) in script change this `"test": "echo \"Error: no test specified\" && exit 1"` with this `"start": "node index.js"` then type in below main `"type": "module",`
<img width="691" height="308" alt="image" src="https://github.com/user-attachments/assets/c2c04c31-dbf1-4009-8ffe-22ec0626abc3" />
     
---
4) create a index.js file in module folder
     
---
5) create a dockerfile then build and run it on locally
<img width="526" height="68" alt="image" src="https://github.com/user-attachments/assets/87e82625-223f-4342-a8b5-6d87618c85c9" />
     
---
6) create docker-compose file to containers and run it `sudo docker-compose up -d` down it `sudo docker-compose down` to check its running locally
     
---

7) make a .github folder and write a workflow file
     
---
8) then push the folder into a git repo

<img width="1278" height="511" alt="image" src="https://github.com/user-attachments/assets/28fc3a46-d63f-4a97-8f42-2cb0e26bbed7" />

---

9) spin up a ec2 ubuntu instance then update and install docker and generate keygen for accessing

   sudo apt-get update
   
   sudo apt-get install ca-certificates curl -y

   sudo install -m 0755 -d /etc/apt/keyrings

   sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc

   sudo chmod a+r /etc/apt/keyrings/docker.asc

   echo \
     "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] \
     https://download.docker.com/linux/ubuntu \
     $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
     sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

    sudo apt update
   
    sudo apt install docker-compose-plugin -y
   
check version

    docker compose version
   
then clone the repo to EC2 Instance  

then build the container

    docker-compose up -d --build

To see changes update something in index.js then push to repo so it reflect in the page directly

   
