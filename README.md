# Docker web app


### About Web App

Its a web app based on flask and it would be running on port 5000.
As part if this I am just printing "Hello world" once we would load the webpage.

##### Steps followed:

###### Prerequisites to follow below steps: 

Python 3.6
Flask
docker

Step 1- Created a flask app: Creted a flask app which is printing "Hello world", it can be seen in file app.py.

Step 2- Created the requirement files which and added packages which needs to be added can be seen in requirements.txt.

Step 3- Cretaed the Dockerfile which contains set of instructions to create docker image of the application, can be seen in Dockerfile.

Step 4- Build the docker image: Creted the docker images using command 
        $ docker image build -t docker-flask-test .
        and it created the image with name docker-flask-test. 
        to verify it we can ran the command 
        $ docker image ls and it should show us our created image with name docker-flask-test.

Step 5- Now run the docker container using command 
        $ docker run -p 5001:5000 -d docker-flask-test which means we're mapping the Python app running on port 5000 inside the container to port 5000 on our host. And now we
        can application by accessing http://localhost:5000/ in our browser.
        
Step 6- After this we can stop it using command 
        $ docker container stop <Container id which we have been got when we had run  $ docker run -p 5001:5000 -d docker-flask-test> also we can remove the stopeed container             using command $ docker system prune if needed.
        
##### Author - M20AIE215
