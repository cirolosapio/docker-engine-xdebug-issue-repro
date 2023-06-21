# Docker Engine + XDebug Repro

Steps to reproduce: 

- `docker compose -f "compose.yml" up -d --build`
- set a breakpoint
- `docker exec -it <container_id> sh`
- `php test.php`