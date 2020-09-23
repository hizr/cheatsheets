# Maven mit abweichender Settings Datei starten
```bash
mvn -s R:\.m2\settings-iJ-c.xml -Pdev-local-compile -T1C clean install
mvn -s R:\.m2s\ettings-iJ-c.xml -Pdev-local-compile -T1C -pl :business-process install -amd
```

# Einzellnen Test starten
```bash
mvn test -Pci -Pintegration-test -Dmaven.test.failure.ignore=true -Dtest=TheTestClassToExecute
```
