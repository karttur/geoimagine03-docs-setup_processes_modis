---
layout: article
title: modis-restoresql_v090.json
categories: setup_processes
excerpt:  Restore the data for the db table for modis.tilecoords from dumped sql
tags:: 
    - json/modis-restoresql
date: 2021-12-04
modified: 2021-12-04
comments: true
share: true
---

# json/modis restoresql (setup_processes)

###  Restore the data for the db table for modis.tilecoords from dumped sql

The json command file <span class='file'>modis-restoresql_v090.json</span> is part of karttur's GeoImagine project <span class='project'>setup_processes</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

```
{
  "userproject": {
    "userid": "karttur",
    "projectid": "karttur",
    "tractid": "karttur",
    "siteid": "*",
    "plotid": "*",
    "system": "system"
  },
  "period": {
    "timestep": "static"
  },
  "process": [
    {
      "processid": "RestoreTableSQL",
      "overwrite": false,
      "version": "0.9",
      "verbose": 2,
      "parameters": {
        "schema": "modis",
        "table": "tilecoords",
        "format": "p",
        "datum": "0",
        "cmdpath": "/usr/local/bin",
        "dataonly": true,
        "definitiononly": false
      },
      "dstpath": {
        "volume": "DEMDATA",
        "hdr": "shp",
        "dat": "shp"
      }
    }
  ]
}
```
