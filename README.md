# docker-tomcat
Here we will see how to set up tomcat in docker.Below are the steps.
* build the image using the Dockerfile from this git
* run the image as container
  * verify if image is running or not
  * verify logs of the container
  * curl to the container
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

