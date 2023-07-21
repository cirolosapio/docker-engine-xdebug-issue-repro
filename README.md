# WSL + Docker Engine + XDebug Repro (NO DOCKER DESKTOP)

This repo was created to reproduce the issue that xdebug does not work with docker engine (no docker desktop) installed following [this guide](https://docs.docker.com/engine/install/ubuntu/)

Steps to reproduce: 

- `docker compose -f "compose.yml" up -d --build`
- set a breakpoint on `test.php`
- start the debug server
- `docker exec -it <container_id> sh`
- `php test.php`

```
Docker version:
Client: Docker Engine - Community
 Version:           24.0.2
 API version:       1.43
 Go version:        go1.20.4
 Git commit:        cb74dfc
 Built:             Thu May 25 21:51:00 2023
 OS/Arch:           linux/amd64
 Context:           default

Server: Docker Engine - Community
 Engine:
  Version:          24.0.2
  API version:      1.43 (minimum version 1.12)
  Go version:       go1.20.4
  Git commit:       659604f
  Built:            Thu May 25 21:51:00 2023
  OS/Arch:          linux/amd64
  Experimental:     false
 containerd:
  Version:          1.6.21
  GitCommit:        3dce8eb055cbb6872793272b4f20ed16117344f8
 runc:
  Version:          1.1.7
  GitCommit:        v1.1.7-0-g860f061
 docker-init:
  Version:          0.19.0
  GitCommit:        de40ad0
```

```
WSL version:
Versione WSL: 1.2.5.0
Versione kernel: 5.15.90.1
Versione WSLg: 1.0.51
Versione MSRDC: 1.2.3770
Versione Direct3D: 1.608.2-61064218
Versione DXCore: 10.0.25131.1002-220531-1700.rs-onecore-base2-hyp
Versione di Windows: 10.0.25393.1
```
