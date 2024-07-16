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
