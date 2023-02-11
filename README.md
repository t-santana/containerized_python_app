# Mimecast DevOps Engineer Codility Test

## Overview

This zip contains two directories both of which accomplish the same outcome although in albeit different steps in the Dockerfile. 

- The Dockerfile in **directory 1** will be using the Python:3.9 image from the Official Python account
- The Dockerfile in **directory 2** will be using a custom image written from me. 

### Requirements

In order for the Dockerfile image to be build correctly the following files must be present in the directories mentioned above along with their respective Dockerfiles: 

- ```requirements.txt```, which contains the dependencies used by the Python Application. 
-  ```python_app.py```, the Python Application to be used during the container run. 

### How-To

In order to build and run the containerized application, please follow the steps here as follow:

#### Build

Do a directory change (`cd` in linux based environments) to the directory where the desired Dockerfile is stored and then run the following command. 

```bash
docker build . -t mimecast_test_container
```
Note: replace `mimecast_test_container` with your desired container name if needed be. 

#### Run it

While on the same directory as the Dockerfile and once the image has been build, run the following command:

```bash
docker run --rm --name mimecast_container -v $PWD:/usr/src/app mimecast_test_container your_number_of_lines
```

Note: You MUST replace `your_number_of_lines` in the above command with an INT value representing the desired number of lines to be printed on the "file_with_lines.txt" file. 

After running the command, the temporary container will be removed and the file "file_with_lines.txt" will be saved in the current directory. 
