Objective:

To complete objectives for this case, you'll need to access and clone the ../app-source-code folder and try to execute different commands

1. Understanding artifacts in an SDLC: 
Artifacts can be documents, architecture diagrams or application binaries, docker images etc. Basically anything that is deliverable to different or same business line.

Thought process:
- What type of artifacts are required in order to run the application
- How we can define the build and release cycles using these artifacts ?
- What gets updates when there is a change in the application ( can be source code change due to new release, can be network change, can be firewall change etc)
- How artifacts differ when it comes to monolith OR a micro-service ?


2. Establish a pipeline/system design to build artifacts in CI (continuous integration) system so that they are available for CD (continuous deployment) system

Thought process:
- Thinking about storing builds or deployable in repositories?
- Prepare the repository ( What are public and private repositories)?
- How will you select the repository for the enterprise ? (think about technologies used and one unified way of creating repo for multiple application)
- Build a CI system? ( build Jenkins or bamboo or something similar), For our exercise bamboo or Jenkins anything can be used or both to learn different ways
- For workshop purpose these systems need to run locally (think about running a Jenkins locally, make sure its data persists with restarts, you can run in docker or a VM)
- To expose your local system accessible over internet you can use a tool like this - https://ngrok.com/ ( think about why would you expose this system over internet? does any outside system requires its presence over a URL that is accessible)
- Build your artifacts (docker images, binaries or similar things that are repeatable and keep changing with application change)
- Try to change a version of your application and build a versioned artifacts in the repository? (Feeling confident?)

3. Don't think about CD yet and read about need of a CI system and prepare notes around why do you need a CI system (maximum five bullet points)

4. Prepare a diagram of above system and keep it in the lucidchart (make sure you involve all teh components involved like Source code repo, CI system, Image or binary repo etc)