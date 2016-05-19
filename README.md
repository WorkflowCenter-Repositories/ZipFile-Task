# SAMTools-Picard-Task
##Repository for SAMTools-index Task of Sequence Cleaning Workflow

###How to deploy the task:  
- Clone this repository to your machine   
- if you want deploy the task with your own data then  
  - in Mega-NJ-Task/input folder put your file, edit Mega-NJ-Task/input.yaml file and change 'input-file' to your file name  
  - in a terminal run . ./task-deploy.sh within Mega-NJ-Task folder  
- if you are happy to deploy the task with the sample input file in input folder just run task-deploy.sh as above  

###Information:  

  Task-Name: SAMTools-index  
  version: 1.0  
  Description: The task implements neighbour joining method. It was designed in the e-Science Central system.  
  task-dependencies: {java1.7, SAMTools-lib}   
  
Blueprint:  
  
  blueprint-name: SAMTools-Picard.yaml  
  Docker-images: dtdwd/samtools1  
  sizes: 228 MB  
  OS-types: ubuntu14.4   
  
Input:  
  
  input-file(s):   
  description:   
  types:   
  
Outputs:  
  
  output-folder: '~/SAMTools-Picard'  
  output-file(s): {}  
  description:  
  types: {}  
  
Execution-Environment:  
  
  Cloudify-version: 3.2  
  Docker-version: 1.8+  
  OS-type: ubuntu14.04  
  Disk-space: 10 GB  
  RAM: 3 GB  
