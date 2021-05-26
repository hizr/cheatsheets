# list all docker images
```bash
docker images
```
# Load an image from file (tar oder img)
```bash
docker load -i <docker-image-file>
```
# start a container
```bash
docker run -d --name local-oracle -p22:22 -p1521:1521 --restart=always <docker-image-id>
```
