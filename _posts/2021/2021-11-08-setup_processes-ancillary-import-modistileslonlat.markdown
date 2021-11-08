---
layout: article
title: ancillary-import-modistileslonlat_v090.json
categories: setup_processes
excerpt:  Import the shape file with the MODIS tile coords in lon lat format
tags:: 
    - ancillary-import-modistileslonlat
date: 2021-11-08
modified: 2021-11-08
comments: true
share: true
---

# ancillary import modistileslonlat (setup_processes)

###  Import the shape file with the MODIS tile coords in lon lat format

The json command file <span class='file'>ancillary-import-modistileslonlat_v090.json</span> is part of karttur's GeoImagine project <span class='project'>setup_processes</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

```
{
  "userproject": {
    "userid": "karttur",
    "projectid": "karttur",
    "tractid": "karttur",
    "siteid": "*",
    "plotid": "*",
    "system": "ancillary"
  },
  "period": {
    "timestep": "static"
  },
  "process": [
    {
      "processid": "OrganizeAncillary",
      "overwrite": false,
      "parameters": {
        "importcode": "shp",
        "epsg": "4326",
        "orgid": "karttur",
        "dsname": "modistiles",
        "dsversion": "1.0",
        "accessdate": "20180908",
        "regionid": "globe",
        "regioncat": "globe",
        "dataurl": "",
        "metaurl": "",
        "title": "SIN modis tiles projected to lonlat",
        "label": "SIN modis tiles projected to lonlat"
      },
      "srcpath": {
        "volume": ".",
        "hdr": "shp",
        "dat": "shp"
      },
      "dstpath": {
        "volume": "geoinfo2021",
        "hdr": "shp",
        "dat": "shp"
      },
      "srcraw": [
        {
          "modtiles": {
            "datadir": "data",
            "datafile": "modtiles_karttur_global_0",
            "datalayer": "tiles",
            "title": "SIN modis tiles projected to lonlat",
            "label": "SIN modis tiles projected to lonlat"
          }
        }
      ],
      "dstcomp": [
        {
          "modtiles": {
            "source": "karttur",
            "product": "modtiles",
            "content": "tiles",
            "layerid": "modtiles",
            "prefix": "modtiles",
            "suffix": "lonlat",
            "dataunit": "tile",
            "celltype": "vector",
            "cellnull": "0",
            "measure": "N",
            "masked": "N"
          }
        }
      ]
    }
  ]
}
```
