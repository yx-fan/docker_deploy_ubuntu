# docker_deploy_ubuntu

### Update package lists to ensure you get the latest version and dependencies
sudo apt update

### Upgrade the system to ensure all packages are up to date
sudo apt upgrade -y

### Install packages to allow apt to use a repository over HTTPS
sudo apt install -y apt-transport-https ca-certificates curl software-properties-common

### Add Docker’s official GPG key
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

### Add the Docker APT repository to your system's software repository list
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"

### Update the package lists again to include packages from the newly added Docker repository
sudo apt update

### Install Docker CE (Community Edition)
sudo apt install -y docker-ce

### Start the Docker service
sudo systemctl start docker

### Enable Docker to start on boot
sudo systemctl enable docker

sudo docker --version
