English | [简体中文](./README.zh-cn.md)

## rancher plugin



https://plugins.jetbrains.com/plugin/19316-rancher



### Basic environment configuration



#### The first step is to download the rancher-cli file

> [rancher-cli distribution download address](https://github.com/rancher/cli/releases)

#### The second step is to download the kubectl file

> [installation tool | Kubernetes](https://kubernetes.io/docs/tasks/tools/)

#### The third step configures environment variables

> Configure rancher and kubectl to the environment variable Path

##### For example, under the window

- rancher file path: C:\userbin\rancher.exe
- kubectl file path: C:\userbin\kubectl.exe
- The environment variables are set as follows

> Path=C:\userbin\


##### For example, under the linux

- download https://dl.k8s.io/release/v1.27.3/bin/darwin/arm64/kubectl Save it to the PATH directory (execute in the terminal to view the corresponding directory: echo PATH)

- https://github.com/rancher/cli/releases Download the corresponding ranger executable file from the download page and also save it in the PATH directory


### For example,under the macos

```
mkdir -p /usr/local/bin
cd /usr/local/bin
# 删除旧文件，请自己备份.Delete old files and back them up yourself
rm -rf  rancher
rm -rf  kubectl


curl -LO https://github.com/rancher/cli/releases/download/v2.6.11/rancher-darwin-amd64-v2.6.11.tar.gz
tar zxvf rancher-darwin-amd64-v2.6.11.tar.gz
cp rancher-v2.6.11/rancher ./
rm -rf rancher-darwin-amd64-v2.6.11.tar.gz

##  for MACOS intel CPU
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/darwin/amd64/kubectl"
## for Apple Silicon CPU
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/darwin/arm64/kubectl"

## 重启一下
reboot
```


#### Operation screenshot

![image-20220623101953105](assets/image-20220623101953105.png)



![image-20220623101928285](assets/image-20220623101928285.png)

#### Click the Detect button in the configuration before adding the account information

![image-20220623101159975](assets/image-20220623101159975.png)



![image-20220623102727662](assets/image-20220623102727662.png)

#### File upload and download

![image-download](assets/download.png)
![image-upload](assets/upload.png)
![image-upload_dirs](assets/upload_dirs.png)
