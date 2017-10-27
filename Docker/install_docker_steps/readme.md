<p align="center">
<h2> Steps for Installing Docker </h2>
</p>

#### First, add the GPG key for the official Docker repository to the system
```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

#### Add the Docker repository to APT sources
```bash
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
```

#### Next, update the package database with the Docker packages from the newly added repo
```bash
sudo apt-get update
```

#### Make sure you are about to install from the Docker repo instead of the default Ubuntu 16.04 repo
```bash
apt-cache policy docker-ce
```

#### Finally, install Docker
```bash
sudo apt-get install -y docker-ce
```

#### Docker should have been installed by now, try following command
```bash
docker --help
```
