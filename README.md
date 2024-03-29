# Simple Flask Web App

This is a basic Flask web application with two routes: index and result.

### Folder Structure:
- `app.py`: Contains Flask application code.
- `templates`: Folder holding HTML templates (index.html, result.html).
- `static`: Folder containing static files (style.css).

### How to Run:
1. Create an EC2 Instance in Ubuntu
2. Install docker on that EC2 instance the commands are
    - sudo apt-get update
    - sudo apt-get install -y docker.io
    - docker --version
    - sudo usermod -aG docker ubuntu 
    - newgrp docker

Create a Dockerfile
===================

3. Create a Dockerfile for the calculator application.

4. Build the image for dockerfile and check size of the docker image it approximately 476MB
    - docker build -t cal-n .

5. create a container on that image with port 5000
    - docker run --name cal-n -d -p 5000:5000 cal-n:latest

6. Access it from the external browser

For multi stage dockerfile
==========================
7. Create a multi stage docker file for the same application

8. Build the image for dockerfile and check size of the docker image it approximately 129MB
    - docker build -t app-n .

9. create a container on that image with port 5000
    - docker run --name app -d -p 5000:5000 app-n:latest

10. Access it from the external browser

==> A multi-stage Dockerfile uses multiple FROM statements to create separate build stages, allowing you to optimize the final image size and improve build efficiency

Enjoy exploring the basic functionalities!

For Build Spec.yml in AWS DevOps Cicd Pipeline --> to provide sensitive info like credentials --> Go to System Manager --> Click on Parameters store on leftside --> create parameters shown in below image. click on create.
![image](https://github.com/Ravindra0849/calculator_application_python/assets/148531100/34f794d3-9ea4-4c39-a69c-ea8f17185b12)
![image](https://github.com/Ravindra0849/calculator_application_python/assets/148531100/71b81dc0-da31-4446-8c54-d3d5b22c1a17)
![image](https://github.com/Ravindra0849/calculator_application_python/assets/148531100/3c8a4f8c-d1d9-474f-ad67-ed95502ac2a2)

