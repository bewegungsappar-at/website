# phail-alarm

repo clonen:
```git clone --recursive $(remote url)```

Als static site generator wird __hugo__ verwendet. Installationsanleitung: https://gohugo.io/getting-started/installing/

Die website wird mit githubpages gehostet, hierfür werden anstelle von __.md__-Dateien HTML,CSS und JavaScript Dateien benötigt. Diese befinden sich im Ordner ```public/```.

Der aktuelle Stand der website wird mit ```hugo -t minimage``` generiert.

Für die Entwicklung, kann mit ```hugo serve -t minimage``` ein lokaler webserver gestaret werden.

Die Datein, welche relevant sind liegen unter ```content/```. Bilder liegen unter ```static/img/```.


____

Die website ist derzeit unter https://bewegungsappar.at erreichbar.

[![Build Status](https://ci.hacknology.de/api/badges/bewegungsappar.at/website/status.svg)](https://ci.hacknology.de/bewegungsappar.at/website)
