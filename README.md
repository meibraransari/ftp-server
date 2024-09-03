---
Created: 2024-07-27T13:55:51+05:30
Updated: 2024-09-03T08:13:06+05:30
Maintainer: Ibrar Ansari
---
# FTP Server (Just in 15 Seconds)

This repository contains information to deploy a FTP server using Docker. The setup includes Demonstration ands steps. The main aim is to quickly Spin Up an FTP Server in Seconds and share data (Upload/Download) easily with Dynamic username and password.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Quick Start](#quick-start)
	- [Change FTP Server Variable](#Change-FTP-Server-Variable)
	- [Run Container](#Run-Container)
- [Connect FTP](#Connect-FTP)
- [Conclusion](#Conclusion)

## 🎬 Video demonstration
[![Watch on Youtube](https://i.ytimg.com/vi/iadE-Px-aYQ/maxresdefault.jpg)](https://youtu.be/iadE-Px-aYQ?si=i9ufOZHcb2msOi8L)

## Prerequisites
- Docker  must be installed on your system.
- Basic understanding of Docker and SFTP.
- Basic knowledge of command-line operations.
## Quick Start
### Change FTP Server Variable

To start a container use the following:
> Change below variable before start it.
```
FTP_CONTAINER_NAME=ftp_server
FTP_USER=user
FTP_PASS=123
FTP_DATA_PATH=/data
```

### Run Container
```sh
docker run -d \
    --name $FTP_CONTAINER_NAME \
    --restart=always \
	--env FTP_PASS=$FTP_PASS \
	--env FTP_USER=$FTP_USER \
	--publish 20-21:20-21/tcp \
	--publish 40000-40009:40000-40009/tcp \
	--volume $FTP_DATA_PATH:/home/user \
	ibraransaridocker/ftp-server
```

### Connect FTP
Configure FileZilla settings before connecting it.
Open FileZilla, Edit > Setting
- FTP
	- Transfer Mode =>Active
	- [✓] Allow fallback to other transfer mode on failure.
		-  Active Mode
			- Limit Local ports by FileZilla
			- Lowest Available Port: 40000
			- Highest Available Port: 40009
			- Ask your operating system for the external IP Address.
		- Passive Mode
			- Fallback to Active Mode.

Connect FTP server using above provided details
Enjoy 😊

### Conclusion
This project streamlines the process of deploying a secure FTP server through Docker. By utilizing Docker, you can achieve faster deployment of FTP Server.


### 💼 Connect with me 👇👇 😊

- 🔥 [**Youtube**](https://www.youtube.com/@DevOpsinAction?sub_confirmation=1)
- ✍ [**Blog**](https://ibraransari.blogspot.com/)
- 💼 [**LinkedIn**](https://www.linkedin.com/in/ansariibrar/)
- 👨‍💻 [**Github**](https://github.com/meibraransari?tab=repositories)
- 💬 [**Telegram**](https://t.me/DevOpsinActionTelegram)
- 🐳 [**Docker**](https://hub.docker.com/u/ibraransaridocker)