## Overview

This repository contains a [MapProxy application](https://mapproxy.org/) for the Datapunt Map project. It provides a UWSGI-based WMTS and WMS server to serve pre-generated tiles from a storage backend (typically an object store).

`mapproxy.yaml` - Mapproxy generic config, this defines the services, sources, caches, layers and globals

## Config files

* `mapproxy.yaml` - MapProxy WMTS config, this defines the service, sources, caches, layers and globals for the WMTS server.
* `mapproxy-seed.yaml` - Defines the sources and caches used in seeding the basiskaarten and luchtfotos.
* `seed.yaml` - MapProxy caching configuration defines the caches to build and their bboxes and zoom levels.

Run this for local development

```bash
    setx OS_URL "t1.data.amsterdam.nl"
    setx MAPSERVER_URL "mapserver_instance_for_reference_map"
    docker compose up
```

This will spawn a MapProxy container that serves WMTS and WMS services from the acceptance object store that contains pre-generated tiles.

## Support

If we need help with MapProxy, we can contact the following person:

Edward Mac Gillavry
webmapper.net