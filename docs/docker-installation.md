# Docker installation

> [Install Docker](https://docs.docker.com/engine/install/ubuntu/)
> [Post Install](https://docs.docker.com/engine/install/linux-postinstall/)

```
sudo apt-get update
```
```
sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release
```
```
sudo mkdir -p /etc/apt/keyrings
```
```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
```
```
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```
```
sudo apt-get update
```
```
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin docker-compose
```
Add your user to docker group and logout.
```
sudo usermod -aG docker $USER
```
Start docker service
```
sudo service docker start
```
Run hello world container
```
docker run hello-world
```
