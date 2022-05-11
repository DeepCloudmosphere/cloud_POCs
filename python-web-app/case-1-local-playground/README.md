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
      ```this application is not required any kind of port binding to run. because to run application simply execute file by python3 on locally that is listen port 5000 by default. ```

- Imp: If application is stateful or stateless? What if the difference?
- Dependency tree for application ( on what other application or distributed systems does it depend on? There can be other services/microservices or DBs probably with whome it interacts?)



## 2. Build application locally to understand the build process and dependencies.

- **Application is dockerized or not?**

  ```No application is not dockerize its just in form of source code.```

- **If the application is not dockerized can we dockerize it or not?**
    ``` 
    Yes, we can dockerize application with two simple steps

          1. Create docker file 
          2. build image with the help of docker file. 
    ```

- **How can we build and test application locally ? Docker compose or similar solution ?**

  ``` Before building application we must have to create a Dockerfile of that application source code.```

  ``` In this case we also take care of security and size of the image by using distroless image  provided by google.```

  - ```security is important because there is always a risk of open vulnerabilities in the base image thats why  using distroless image is better choice. ```

  - ```“Distroless” images contain only your application and its runtime dependencies. They do not contain package managers, shells or any other programs you would expect to find in a standard Linux distribution.```

  ```Now, We can use a `multi-stage`  build docker file to run our production containers with a distroless image.```

    - ```Multi-stage builds in our Dockerfile allow for as many stages of the build process. We can daisy-chain the outputs of one stage as inputs to the next stage. The only expectation is that the last stage will be our production stage with the distroless image.```



![Screenshot 2022-05-11 at 11 16 01 PM](https://user-images.githubusercontent.com/98619865/167915545-27084b3f-d85b-4c6a-910c-976b5ac30c76.png)




  ```By default, many containers are configured to execute as root, which is needed to install packages and make configuration settings. But after all that is done, we can change to a non-root user. distroless image is already included nonroot user (65532:65532).```



  ----------Build image by `docker image build -t <tag>` or `docker build -t <tag>` command----------
  
  ![Screenshot 2022-05-11 at 11 39 57 PM](https://user-images.githubusercontent.com/98619865/167918061-8e664c68-7e6f-4a76-b84c-81cf699e4a01.png)


------------check image by `docker images` command --------------

    - You can see image name is `deepcloudmosphere/python-web` with tag name `distroless`

 ![Screenshot 2022-05-11 at 11 45 28 PM](https://user-images.githubusercontent.com/98619865/167918736-a4b1b5fe-ebac-488f-864e-4551050ad748.png)


  ----------Finally test application by `docker container run -p 3333:5000  deepcloudmosphere/python-web:distroless` command ----------

![Screenshot 2022-05-11 at 11 46 44 PM](https://user-images.githubusercontent.com/98619865/167919394-75b78bab-0a4c-492a-bc59-c18f04723ef8.png)


3. Understand success criteria if our application is able to run successfully on local machines

Thought process:
- Try to interact with the service?
- Start/Stop/Restart to check the behaviors and note them down?
- Check the logs from the service? Are logs written to a file or stdout of a container?

Prepare a document and note down your understanding about different aspects of this application. remember, you can always be creative with diagrams.

