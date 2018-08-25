# docker-tomcat
Here we will see how to set up tomcat in docker.Below are the steps.
* build the image using the Dockerfile from this git
* run the image as container.
  * verify if image is running or not.
  * verify logs of the container.
  * curl to the container from host.
  * get into the container and curl the tomcat end-point.
* remove resources
  * stop the container
  * remove the container
  * remove the image

Build The Image Using Dockerfile
--------------------------------
* clone this git repo. open terminal and go to the repository directory where you will find Dockerfile
* command to list the files: `ls`
![image](https://user-images.githubusercontent.com/17001948/44620143-f864d880-a8ac-11e8-9876-f5e4caa927af.png)
* build image command: `sudo docker build -t my-tomcat-image .`
![image](https://user-images.githubusercontent.com/17001948/44620163-29450d80-a8ad-11e8-9439-08dabb8d27c2.png)
* While the above command ix executing to build the image you can see below screenshot.
![image](https://user-images.githubusercontent.com/17001948/44620171-542f6180-a8ad-11e8-8125-498d0a9fd226.png)
* Image created successfully
![image](https://user-images.githubusercontent.com/17001948/44620215-06672900-a8ae-11e8-960d-0a1205436570.png)
* View image: `sudo docker images`
![image](https://user-images.githubusercontent.com/17001948/44620235-4e864b80-a8ae-11e8-8dd5-78a66040a607.png)

Run The Image As Container
--------------------------
* run command: `sudo docker run --rm --name my-container-c -d -p 8081:8080 my-container-image`
![image](https://user-images.githubusercontent.com/17001948/44620283-0582c700-a8af-11e8-947b-5aab69e33485.png)
* container created.
![image](https://user-images.githubusercontent.com/17001948/44620294-32cf7500-a8af-11e8-9203-1dbc137d9f86.png)
* see container is running: `sudo docker ps`
![image](https://user-images.githubusercontent.com/17001948/44620298-572b5180-a8af-11e8-8588-836ac9391f26.png)
* check logs. command : `sudo docker logs my-container-c`
![image](https://user-images.githubusercontent.com/17001948/44620324-d3be3000-a8af-11e8-9f06-1e7d00d69974.png)
* Above command will show tomcat logs.
![image](https://user-images.githubusercontent.com/17001948/44620327-e9cbf080-a8af-11e8-93c7-2d4b3fd7042b.png)
* use curl command to interact with the tomcat. command: `curl http://localhost:8081`
![image](https://user-images.githubusercontent.com/17001948/44620333-0bc57300-a8b0-11e8-9f33-8cb9ceb4aee4.png)
* Above will show the html response of index page of tomcat.
![image](https://user-images.githubusercontent.com/17001948/44620350-44654c80-a8b0-11e8-8f23-9d1dd55d3410.png)
* Access it from browser.[See I am using ubuntu terminal.].
![image](https://user-images.githubusercontent.com/17001948/44620357-71b1fa80-a8b0-11e8-9c4d-bd32bf0d4a31.png)
* Get into the container. command: `sudo docker exec -it my-tomcat-c bash`
![image](https://user-images.githubusercontent.com/17001948/44620487-b9398600-a8b2-11e8-9484-185a4fb3a5b9.png)
* Now curl to the tomcat end point. command: 
![image](https://user-images.githubusercontent.com/17001948/44620492-db330880-a8b2-11e8-93a6-29584868c7ff.png)
* Above command will show the tomcat logs.
![image](https://user-images.githubusercontent.com/17001948/44620496-f140c900-a8b2-11e8-8865-1dbb7d410db3.png)


