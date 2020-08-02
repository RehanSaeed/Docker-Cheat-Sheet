# Docker-Cheat-Sheet

A cheat sheet for Docker commands.

## buildx

| Command                                                                                                             | Description                      |
| ------------------------------------------------------------------------------------------------------------------- | -------------------------------- |
| `docker buildx version`                                                                                             | The version of buildx            |
| `docker pull -q multiarch/qemu-user-static:latest`                                                                  | Pull & install latest QEMU image |
| `docker run --rm --privileged multiarch/qemu-user-static:latest --reset -p yes --credential yes`                    |                                  |
| `docker buildx create --name builder --driver docker-container --use`                                               | Create buildx instance           |
| `docker buildx inspect --bootstrap`                                                                                 |                                  |
| `docker buildx build --platform "linux/amd64,linux/arm64" --progress plain --tag test --file "C:\Foo\Dockerfile" .` | Build an image                   |

## Redis

```powershell
docker run --name redis -p 6379:6379 -d --restart unless-stopped redis

docker exec -it redis redis-cli
```
