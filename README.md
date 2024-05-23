# Simple Notes App
This is a simple notes app built with React and Django.

## Requirements
1. Python 3.9
2. Node.js
3. React

## Installation
1. Clone the repository
```
git clone https://github.com/LondheShubham153/django-notes-app.git
```

2. Build the app
```
docker build -t notes-app .
```

3. Run the app
```
docker run -d -p 8000:8000 notes-app:latest
```

## Nginx

Install Nginx reverse proxy to make this application available

`sudo apt-get update`
`sudo apt install nginx`


# Perform CI/CD using Jenkins Pipeline
Use Declarative checkout means Jenkins uses Jenkinsfile in which the pipeline is defined and the file is hosted on SCM platforms like GitHub in the root folder of the project.

Follow the below steps to implement the Declarative checkout
1) In Build Triggers section select the GitHub hook trigger for GITScm polling option
![image](https://github.com/jayeshrajputtech/django-react-notes-app/assets/166933906/7400f262-91a9-4dee-9d79-8828f9b531ec)

2) In Pipeline section in Definition option select the Pipeline script from SCM option and in the SCM select Git. Provide the Repository URL and credentials if any.
![image](https://github.com/jayeshrajputtech/django-react-notes-app/assets/166933906/cc0d2f4f-fa9b-487f-a387-e6ff9638bc7c)

3) Mention the correct branch in which the code and Jenkinsfile is present and in the Script Path option mention Jenkinsfile if it is present in the root directory of the project if not the specify the path of the Jenkinsfile then click on save button to save the changes.
![image](https://github.com/jayeshrajputtech/django-react-notes-app/assets/166933906/32deac04-129f-46d4-a09a-960a298e5367)

4) Click on the Build Now button to execute the pipeline. The pipeline code or definition will be picked from the SCM GitHub repository
