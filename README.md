# ZipFile-Task
##Repository for ZipFile Task 

###How to deploy the task:  
- Clone this repository to your machine   
- if you want deploy the task with your own data then  
  - in ZipFile-Task/input folder put your file, edit ZipFile-Task/input.yaml file and change 'input-file' to your file name  
  - in a terminal run . ./task-deploy.sh within ZipFile-Task folder  
- if you are happy to deploy the task with the sample input file in input folder just run task-deploy.sh as above  

###Information:  

  Task-Name: ZipFile  
  version: 1.0  
  Description: The task implements zipping a file  
  task-dependencies: {java1.7}   
  
Blueprint:  
  
  blueprint-name: ZipFile.yaml  
  Docker-images: dtdwd/filezip1  
  sizes: 228 MB  
  OS-types: ubuntu14.4   
  
Input:  
  
  input-file(s): file1    
  description: any file to be zipped
  types: any type
  
Outputs:  
  
  output-folder: '~/ZipFile'  
  output-file(s): {}  
  description: a zipped file
  types: zip  
  
Execution-Environment:  
  
  Cloudify-version: 3.2  
  Docker-version: 1.8+  
  OS-type: ubuntu14.04  
  Disk-space: 10 GB  
  RAM: 3 GB  
