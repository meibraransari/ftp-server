---
Created: 2024-07-27T13:55:51+05:30
Updated: 2024-08-31T23:07:33+05:30
Maintainer: Ibrar Ansari
---
# FTP Server

A simple FTP server, using docker to share data (Upload/Download) easily.

## How to use this image

### Start a FTP Server instance

To start a container use the following:

> Change below variable before start it.
```
FTP_CONTAINER_NAME=ftp_server
FTP_USER=user
FTP_PASS=123
FTP_DATA_PATH=/data
```

## Run Container
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

## Connect FTP 
Configure FileZilla settings before connecting it.
Open FileZilla, Edit > Setting
- FTP
	- Transfer Mode =>Active
	- [✔] Allow fallback to other transfer mode on failure.
		-  Active Mode
			- Limit Local ports by FileZilla
			- Lowest Available Port: 40000
			- Highest Available Port: 40009
			- Ask your operating system for the external IP Address.
		- Passive Mode
			- Fallback to Active Mode.

Connect FTP server using above provided details
Enjoy 😊

### 💼 Connect with me 👇👇 😊

- 🔥 [**Youtube**](https://www.youtube.com/@DevOpsinAction?sub_confirmation=1)
- ✍ [**Blog**](https://ibraransari.blogspot.com/)
- 💼 [**LinkedIn**](https://www.linkedin.com/in/ansariibrar/)
- 👨‍💻 [**Github**](https://github.com/meibraransari?tab=repositories)
- 💬 [**Telegram**](https://t.me/DevOpsinActionTelegram)
- 🐳 [**Docker**](https://hub.docker.com/u/ibraransaridocker)