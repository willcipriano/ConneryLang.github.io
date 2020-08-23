# Building and Running

# Build a local Docker image
Another way is to build your own Docker image. Here is how I accomplish that on my local machine, on Windows/Mac you should be able to do something similar.
```
1. git clone https://github.com/willcipriano/Connery.git
2. cd Connery
3. docker build --tag connery .
4. docker run -it connery
```
You should end up with something like this:


<p><img src="/img/connery_docker.JPG"></p>

# Linux
In order to build Connery on Linux (this guide assumes Debian Buster) you will need to install the prerequisites, run the commands below:

```
1. apt-get update
2. apt-get -y install build-essential
3. apt-get -y install cmake
4. apt-get -y install libcurl4-openssl-dev
5. apt-get -y install libedit-dev
6. git clone https://github.com/willcipriano/Connery.git
7. cd Connery
8. cmake .
9. ./cmake-build-debug/Connery
```