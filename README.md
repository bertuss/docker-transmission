# Build

```bash
make build
```
__or__
```bash
docker build --rm --no-cache --pull  -t bertuss/transmission .
```

# Run

```bash
docker run \
    -d \
    --name transmission \
    -p 8080:9091 \
	-v /host/watch:/watch \
	-v /host/downloads:/downloads \ 
	-v /host/incomplete:/incomplete \ 
	-v /host/.config:/config \
    -e USERNAME=username \
    -e PASSWORD=password \
    -e DEBUG=true \
    bertuss/transmission
```