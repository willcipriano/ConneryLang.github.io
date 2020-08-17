# Building and Running

# Docker
The fastest way to get up and running is to use Docker to build and run Connery. Here is how I accomplish that on my local machine, on Windows/Mac you should be able to do something similar.
1. _git clone https://github.com/willcipriano/Connery.git_
2. _cd Connery_
3. _docker build --tag connerylang ._
4. _docker run -it connerylang_

You should end up with something like this:

<p><img src="/img/connery_docker.JPG"></p>

# Linux
In order to build Connery on Linux (this guide assumes Debian Buster) you will need to install the prerequisites, run the commands below:

1. _apt-get update_
2. _apt-get -y install build-essential_
3. _apt-get -y install cmake_
4. _apt-get -y install libcurl4-openssl-dev_
5. _apt-get -y install libedit-dev_
6. _git clone https://github.com/willcipriano/Connery.git_
7. _cd Connery_
8. _cmake ._
9. _./cmake-build-debug/Connery_