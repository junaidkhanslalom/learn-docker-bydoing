# learn-docker-bydoing

## Chapter 2: Docker Basics
1. Initializing the Docker Environment
    1. Install Docker
        1. Install docker prereq: 
        ### sudo yum install -y yum-utils device-mapper-persistent-data lvm2
        2. Using yum-configure-manager add CentoS to specefic repo
        ### sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
        3. Install Docker
        ### sudo yum -y install docker-ce
    2. Enable the Docker System
        1. Enable the Docker daemon: 
        ### sudo systemctl enable --now docker
    3. Configure User Permissions
        1. Add a lab user to the docker group
          ###  sudo usermod -aG docker cloud_user
    4. Run a test image
     ###   docker run hello-world
2. Working With Prebuilt Docker
3. Handcrafting a Container Image
   1. sub-item 1 of item 3
   2. sub-item 2 of item 3