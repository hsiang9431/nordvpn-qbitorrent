# nordvpn-qbitorrent
nordvpn and qbitorrent in docker


## Setup

### Docker Desktop

Download and install Docker Desktop

https://www.docker.com/products/docker-desktop/

### NordVPN Access Token

Create access token: https://support.nordvpn.com/hc/en-us/articles/20286980309265-How-to-use-a-token-with-NordVPN-on-Linux

In `docker-compose.yml`, add your nordvpn token to `NORDVPN_TOKEN`

```yaml
environment:
  NORDVPN_TOKEN: "<add access token here>"
```

### Download folder

In `docker-compose.yml`, change download location in volume setting

```yaml
volumes:
  - C:\Downloads:/etc/qBittorrent/downloads
```

## Start/Stop service

Use `docker-compose.exe` to start service. This exe file comes with Docker Desktop on Windows.

```
PS D:\github\nordvpn-qbitorrent> docker-compose.exe up -d
```

or stop service

```
PS D:\github\nordvpn-qbitorrent> docker-compose.exe stop
```


## Access `qBitorrent` WebUI

`qBitorrent` WebUI is available on `http://localhost:8080`


## Reference

https://github.com/bubuntux/nordvpn/blob/master/Dockerfile

https://support.nordvpn.com/hc/en-us/articles/20465811527057-How-to-build-the-NordVPN-Docker-image

https://linuxcapable.com/how-to-install-qbittorrent-on-ubuntu-linux/

https://github.com/qbittorrent/qBittorrent/issues/8514
