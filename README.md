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
docker run --name redis -p 6379:6379 -d --restart=unless-stopped redis

docker exec -it redis redis-cli
```

## Jaeger

- 55680 - OTLP receiver
- 16686 - Dashboard
- 13133 - Health Check

```powershell
docker run --name jaeger -p 13133:13133 -p 16686:16686 -p 55680:55680 -d --restart=unless-stopped jaegertracing/opentelemetry-all-in-one
```
