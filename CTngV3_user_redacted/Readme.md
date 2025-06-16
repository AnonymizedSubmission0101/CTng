
# CTng: Certificate and Revocation Transparency

This is a Proof of Concept/Prototype code for Periodic Consistent Broadcast Protocol in CTng. Each entity can be found in their corresponding folder.

## Software Requirements (for local testing)

- Ubuntu 22.04
- Golang 1.23
- g++ (Ubuntu 11.3.0-1ubuntu1~22.04.1) 11.3.0
- tmux terminal multiplexer

## Running Tests Locally 

#### Change the variables in the def/testsettings.json file.
#### Modify the run.sh file to run more entities. 

And execute 
 ```
sh run.sh 
 ```
in the project root directory 

## Running Tests with Deterlab TestBed (Sphere Research infrasture)

Please refer to 

https://github.com/AnonymizedSubmission0101/CTngOnSphere/tree/main/CTng-on-Sphere_final_redacted

Link to the testbed: 

https://launch.sphere-testbed.net/


## Disclaimer: 
### 1. 1. Only the logger-related functionalities are actively maintained.
This is because with a lower MMD, the logger becomes the primary bottleneck — it must keep up with the global precertificate generation rate. In contrast, revocation processing does not significantly burden the monitor, as the CRV structure requires only one bit per revoked certificate pre-compression. However, for transparency updates, the monitor must verify every individual certificate, making logger performance more critical.
### 2. This repository does not simulate Specific Logger/CA misbehaviors. 
