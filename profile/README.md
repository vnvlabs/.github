# The VnV Toolkit Project:

VnV Toolkit is a C++ API and Runtime that can be used to add support for end-user verification and validation within scientific applications. 
The toolkit uses a performant MACRO based system and Plugin API to provide a number of features that will allow the USERS of the DEVELOPERS 
application to ANALYZE, VERIFY and VALIDATE the results produced by the given application. 

The VnV toolkit uses DATA extracted during the simulation to generate an interactive SIMULATION REPORT that summarizes the results of simulation.
The toolkit supports the full range of VERIFICATION AND VALIDATION PROCESSES:

Features include:
   - A Builtin Unit Testing Framework.
   - Function level Integration Testing (configurable at runtime by the end-user).  
   - Application level Integration Testing.
   - Provenance Tracking. 
   - Input file validation
   - Live Data Visualization using real simulation data. 
   - Performance Monitoring   
   - Uncertainty Quantification and Sensitivity Analysis
   - A Browser based Execution and Report Viewing GUI.  
 
The toolkit includes an extensive Browser based GUI for simulation design, execution and analysis: The features of the GUI include:

  - Input file GUI including live validation and autocomplete. 
  - Remote Execution using SSH.
  - A fully featured IDE built using Eclipse Theia. 
  - 3D visualization using Paraviewweb.
  - View Live Interactive Simulation reports
  - Supports multi-user  SAAS deployment using Docker. 

## Try it out:

### A Simple Demo Application.

The following docker command will launch a VnV container running on localhost pre installed with 
a range of VnV Applications. . You can navigate to localhost:5001 in the browser to see the GUI. 

    docker run --rm -it -p 5001:5001 ghcr.io/vnvlabs/all /vnv-gui/run.sh

Notes:
   1. The GUI runs inside a docker container where you (the user) has root access. You are logged in as root!
   2. All the source code for the various applications are in /source/* . Software with an install step was in installed in /software/*
   3. Your container will cease to exist as soon as you exit the docker run command. This is just for demo purposes. 

### Software As A Service
   
The following command will deploy the VnV Toolkits SAAS container wrapper. This wrapper lets users create and use containers 
prebuilt using VnV software. It is a really basic html front-end and flask based reverse proxy that allows users to manage the spinning 
up and shutting down of containers. 

    docker run --rm -it --network="host" -v /var/run/docker.sock:/var/run/docker.sock ghcr.io/vnvlabs/serve

Notes:
   1. The default username is Admin. The password will be printed to standard out during initialization. 
   2. The container uses a docker-in-docker scheme to launch containers on behalf of the users. 
   3. When you exit the container, all user information will be lost --- BUT -- Any containers created by the container while it was alive will still be active. All containers launched by this application are given the prefix "vnv-"
   4. The container also allows users to snapshot a container. The images that result from this snapshot will exist beyond the end of the container. You will need to delete those manually. They also all have the prefix "vnv-"
   5. A universal volume is created for each user. This volume is mounted in the /data/ directory of every container launched by the user. This lets users transfer data between containers instantly. 
   6. All the containers run on the same machine -- the machine that is hosting the webserver. In the future, the SAAS deployment will support docker swarm and/or kubernetes to run containers using remote resources.
   7. Each User is given an account balance of $100 when they create an account. THIS BALANCE IS FAKE. It is just there as a mechanism for demostrating the containers abilitiy to track the uptime of each users containers. 
