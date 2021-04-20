

### The Task describes:  

### Python/Flask Application with MongoDB and a Nginx.  
Project structure:   
``` 
.  
├── docker-compose.yaml  

├── flask  

│   ├── Dockerfile  


│   ├── requirements.txt  

│   └── server.py  


└── nginx  

    └── nginx.conf  
```  
The Docker-compose file defines an APP with three services: web (Nginx), backend (Flask) and Database (Mongo). When deploying the application, docker-compose maps port 80 of the web service container to port 80 of the host as specified in the Docker compose file.  

1.	Connect the VM via SSH  

2.	Clone the repo.  

3. 	Deploy the APP with Docker-compose . 

## Expected result  

  Listing containers must show three containers running:  

```  

$ docker ps  
CONTAINER ID        IMAGE                        COMMAND                  CREATED             STATUS              PORTS                  NAMES  
467f0163b5d7        int-exam_backend    "./server.py"            8 seconds ago        Up 7 seconds                             int-exam_backend_1
baa1ef282968        nginx               "/docker-entrypoint.…"   About a minute ago   Up 7 seconds        0.0.0.0:80->80/tcp   int-exam_web_1
a70b8ad151fa        mongo               "docker-entrypoint.s…"   About a minute ago   Up 7 seconds        27017/tcp            int-exam_mongo_1

```  
After the application starts, navigate to `http://SERVER-IP:80` in your web browser:  
``` 
Hello, From, the Tevel's MongoDB client! 
```  
 
 
