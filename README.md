

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

After the application starts, navigate to `http://SERVER-IP:80` in your web browser:  
``` 
Hello, From, the Tevel's MongoDB client! 
```  
 
 
