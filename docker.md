# Alle Docker Images anzeigen
```bash
docker images
```
# Load an image from file (tar oder img)
```bash
docker load -i <docker-image-file>
```
# Container starten
```bash
docker run -d --name local-oracle -p22:22 -p1521:1521 --restart=always <docker-image-id>
```
