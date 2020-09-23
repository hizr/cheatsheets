# Alle Docker Images anzeigen
```bash
docker images
```

# Container starten
```bash
docker run -d --name local-oracle -p22:22 -p1521:1521 --restart=always <docker-image-id>
```