---
Created: 2024-07-27T13:55:51+05:30
Updated: 2024-07-27T13:56:17+05:30
Maintainer: Ibrar Ansari
---
# FTP Server

A simple FTP server, using docker to share data (Upload/Download) easially.

## How to use this image

### Start a FTP Server instance

To start a container, with data stored in `/data` on the host, use the
following:

```sh
docker run \
	--detach \
	--env FTP_PASS=123 \
	--env FTP_USER=user \
	--name my-ftp-server \
	--publish 20-21:20-21/tcp \
	--publish 40000-40009:40000-40009/tcp \
	--volume /data:/home/user \
	ibraransaridocker/ftp-server
```


### 💼 Connect with me 👇👇 😊

- 🔥 [**Youtube**](https://www.youtube.com/@DevOpsinAction?sub_confirmation=1)
- ✍ [**Blog**](https://ibraransari.blogspot.com/)
- 💼 [**LinkedIn**](https://www.linkedin.com/in/ansariibrar/)
- 👨‍💻 [**Github**](https://github.com/meibraransari?tab=repositories)
- 💬 [**Telegram**](https://t.me/DevOpsinActionTelegram)
- 🐳 [**Docker**](https://hub.docker.com/u/ibraransaridocker)