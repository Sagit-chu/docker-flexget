# Docker-flexget

Dockerfile: [https://github.com/Sagit-chu/docker-flexget](https://github.com/Sagit-chu/docker-flexget)

docker-compose


```

version: '3.7'
services:
  flexget:
    image: 601096721/flexget
    container_name: flexget
    environment:
      #密码需保证复杂度
      FG_WEBUI_PASSWD: <password>
      TZ: Asia/Shanghai
      PUID: 1000
      PGID: 1000
    volumes:
      - <path for config files>:/config
      - <path for data files>:/downloads
    ports:
      - "3539:3539"
```