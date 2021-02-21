![](../../resources/logos.png)

----
## Jenkins Labs - Run Jenkins Server (CASC)

[![Open in Cloud Shell](https://gstatic.com/cloudssh/images/open-btn.svg)](https://console.cloud.google.com/cloudshell/editor?cloudshell_git_repo=https://github.com/nirgeier/JenkinsLabs)

### **<kbd>CTRL</kbd> + click to open in new window**   

---

## Preface
- For this demo we will use Jenkins with docker container. 
- Our image is build upon `jenkinsci/blueocean` and is pre-configured using `Jenkins Configuration as Code` [casc.yaml](./jenkins-casc-server/jenkins-casc.yaml) 

<!-- inPage TOC start -->

---
## Lab Highlights:
- [01. Start Jenkins with pre defined docker-compose file](#01-Start-Jenkins-with-pre-defined-docker-compose-file)
- [02. Test Jenkins](#02-Test-Jenkins)

---

<!-- inPage TOC end -->
### 01. Start Jenkins with pre defined docker-compose file
```sh
# Navigate to the custom image folder
cd ./Jenkins-casc-server

# Build and run the custom image
docker-compose up -d --build 
```
### 02. Test Jenkins
- In the previous labs we had to take some manual steps before we were able to use Jenkins.
- in this demo Jenkins will be up and running once the docker-compose has completed
- Wait for the server to load and than open your browser at port 8888 (The port is defined inside the [.env](./Jenkins-casc-server/.env))
```sh
## .env
...
# Listen on the desired ports
# - Port 8888   exposes the web interface 
HOST_PORT_WEB=8888
```