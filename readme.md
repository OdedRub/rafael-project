DevOps Exercise

You are an advanced lifeform from the planet Kepler-186f, you were on an expedition to earth to explore and understand the primitive lifeform called Terran (humans) but your spaceship crashed somewhere in the continent called by the natives North America.
Your mission, if you choose to accept it, is to find one of these primitive terminals called computers, connect to their largest code repository (we believe it’s called GitHub) on their so called “Internet” build a simple hello-world program which through it you’ll be able to signal us to come and pick you up and take you back to your home planet.

In order to get back home you must complete the following tasks:

    1. Fork the following repository https://github.com/ido83/maven-hello-world
    if you don’t know what fork is google it, apparently, they have a primitive yet quite an efficient device which could answer most of your questions, it’s called Google!
    
    2. Understand this repository -
    
        a. Which programming language is this?
        
        b. What is maven? 
        
        c. How does maven work? 
        
        d. What is this pom.xml everyone keeps mentioning?
    
    3. In order to build the above repository, use Azure Pipelines or GitHub Actions. 
    Hint: GitHub Actions is easier
    
    4. Change the code:
    
        a.  Add your name to the "Hello World" message.
        
        b. Set  Jar version to 1.0.0
    
    5. Create a simple pipeline which would do the following actions:
    
        a. Increase the Patch part of the jar version ( 1.0.0 - > 1.0.1) automatically
        
        b. Compile the code
        
        c. Package it into an artifact
        
        d. Create an artifact item for the build
        
        e. Create a docker image  containing the artifact  - use Dockerfile:
        
            i. Tag the Docker image as the the Jar version automatically.
            
            ii. The  Docker image shouldn't run with root
            
        f. Push the docker image that was created in the previous step to Docker Hub
        
        g. Download and run the docker image.
    
    6. Once it’s running, we would come and pick you up immediately

Bonus – do as much as possible from the above using Multistage Docker.

If you encounter any issues with these primitive technologies, we highly recommend using Google, we believe you’ll be able to get most of the answers from this tool.

Good Luck!
