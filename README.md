# docker_deploy_ubuntu

### Update package lists to ensure you get the latest version and dependencies
```bash
sudo apt update
```

### Upgrade the system to ensure all packages are up to date
```bash
sudo apt upgrade -y
```

### Install packages to allow apt to use a repository over HTTPS
```bash
sudo apt install -y apt-transport-https ca-certificates curl software-properties-common
```

### Add Docker’s official GPG key
```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

### Add the Docker APT repository to your system's software repository list
```bash
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
```

### Update the package lists again to include packages from the newly added Docker repository
```bash
sudo apt update
```

### Install Docker CE (Community Edition)
```bash
sudo apt install -y docker-ce
```

### Start the Docker service
```bash
sudo systemctl start docker
```

### Enable Docker to start on boot
```bash
sudo systemctl enable docker
```

```bash
sudo docker --version
```
