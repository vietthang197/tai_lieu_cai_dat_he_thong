# Cách cài đặt docker trên centos
 * Gỡ cài đặt bản docker cũ:
```shell
 sudo yum remove docker \
                  docker-client \
                  docker-client-latest \
                  docker-common \
                  docker-latest \
                  docker-latest-logrotate \
                  docker-logrotate \
                  docker-engine
 ```
 * Set up the repository:
```shell
sudo yum install -y yum-utils
```
```shell
sudo yum-config-manager \
    --add-repo \
    https://download.docker.com/linux/centos/docker-ce.repo
```
 * Install Docker Engine:
```shell
sudo yum install docker-ce docker-ce-cli containerd.io
```
 * Start Docker:
```shell
sudo systemctl start docker
```
 * Để docker tự động start khi server reboot, dùng lệnh:
```shell
sudo systemctl enable docker
```
 * Để chạy các lệnh của Docker bằng account non root như appgw (hoặc kể cả bất kỳ service nào như jenkins,...)
 thì ta phải add user vào group docker. 
```shell
sudo usermod -aG docker $USER
```