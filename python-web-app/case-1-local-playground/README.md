Objective:

To complete objectives for this case, you'll need to access and clone the ../app-source-code folder and try to execute different commands

1. To understand and list down application requirements

Thought process:
- Which language/languages are used in the source code
- Are there multiple services that are packaged in the app ?
- Is it a monolith OR a microservice ? How can one differentiate them ?
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