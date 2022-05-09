# Objective:

To complete objectives for this case, you'll need to access and clone the ../app-source-code folder and try to execute different commands

## 1. To understand and list down application requirements
- **Which language/languages are used in the source code**

   ```This application source code  is using python language```
   
- **Are there multiple services that are packaged in the app?**
    
   ```Yes, there is a Mysql backend service that is packaged within the python source code  for read and write data from database.```
   
- **Is it a monolith OR a microservice ? How can one differentiate them ?**

   ```Yes it is a monolithic application.```
   
  **Differentiate** 
    
  ``` In monolithic all the functionalities of a project exist in a single codebase that is tightly coupled.```
   
   ![image](https://user-images.githubusercontent.com/98619865/167298363-43fbf490-c2fc-4b07-afd4-9bfaea542691.png)
   
   ```But in microservice application is built as independent components that run each application process or functionality as a service and each service communicate each other via http or other lightweight protocol.```
    
   ![image](https://user-images.githubusercontent.com/98619865/167298374-21cb8864-9028-4818-8f4d-0ceabe3ef87e.png)
    

- **What are the networking requirements for the app ?**

    - Is it a batch job that runs in the background linux process?

        ```No, it is not a batch job because ,a batch job is a scheduled program that is assigned to run on a computer without further user interaction.```

        ```This is synchronous task and it is fine when a user needs the result of calculation immediately.``` 

        ```Another use case is when the result is not relevant right now and the user just wants to schedule an execution of the task asynchronously that are run in background in linux process.```

    - Does it listen or expose any information on a port?

      ```this application is not exposing or documenting any port it just listen  on  port 5000 for flask  and 3306 for mysql database  by default.```
      
    - What kind of port binding is required for it to run?
    
      ```this application is not required any kind of port binding to run. because to run application simply execute file on locally that is listen port 5000 by default. ```





- Imp: If application is stateful or stateless? What if the difference?
- Dependency tree for application ( on what other application or distributed systems does it depend on? There can be other services/microservices or DBs probably with whome it interacts?)

2. Build application locally to understand the build process and dependencies

Thought process:
- Application is dockerized or not?
- How can we build and test application locally ? Docker compose or similar solution ?
- If application is not dockerized can we dockerize it or not?
- If application runs as binary on linux can we test it on Virtualbox using Vagrant?
- If application runs as binary can we write a service file (ref: https://www.digitalocean.com/community/tutorials/how-to-use-systemctl-to-manage-systemd-services-and-units)

3. Understand success criteria if our application is able to run successfully on local machines

Thought process:
- Try to interact with the service?
- Start/Stop/Restart to check the behaviors and note them down?
- Check the logs from the service? Are logs written to a file or stdout of a container?

Prepare a document and note down your understanding about different aspects of this application. remember, you can always be creative with diagrams.
- What is the networking requirements for the app ?
    - Is it a batch job that runs in the background linux process? 
    - Does it listen or expose any information on a port?
    - What kind of port binding is required for it to run?
- Imp: If application is stateful or stateless? What if the difference?
- Dependency tree for application ( on what other application or distributed systems does it depend on? There can be other services/microservices or DBs probably with whome it interacts?)

2. Build application locally to understand the build process and dependencies

Thought process:
- Application is dockerized or not?
- How can we build and test application locally ? Docker compose or similar solution ?
- If application is not dockerized can we dockerize it or not?
- If application runs as binary on linux can we test it on Virtualbox using Vagrant?
- If application runs as binary can we write a service file (ref: https://www.digitalocean.com/community/tutorials/how-to-use-systemctl-to-manage-systemd-services-and-units)

3. Understand success criteria if our application is able to run successfully on local machines

Thought process:
- Try to interact with the service?
- Start/Stop/Restart to check the behaviors and note them down?
- Check the logs from the service? Are logs written to a file or stdout of a container?

Prepare a document and note down your understanding about different aspects of this application. remember, you can always be creative with diagrams.
