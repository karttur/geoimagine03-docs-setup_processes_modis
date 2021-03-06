---
layout: article
title: modis-search_datapool_v090.json
categories: setup_processes
excerpt:  Search LPDAAC datapool for MODIS tiles
tags:: 
    - json/modis-search_datapool
date: 2021-12-04
modified: 2021-12-04
comments: true
share: true
---

# json/modis search datapool (setup_processes)

###  Search LPDAAC datapool for MODIS tiles

The json command file <span class='file'>modis-search_datapool_v090.json</span> is part of karttur's GeoImagine project <span class='project'>setup_processes</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

```
{
  "userproject": {
    "userid": "karttur",
    "projectid": "karttur",
    "tractid": "karttur",
    "siteid": "*",
    "plotid": "*",
    "system": "modis"
  },
  "period": {
    "startyear": "2018",
    "endyear": "2020",
    "timestep": "8D"
  },
  "process": [
    {
      "processid": "searchDataPool",
      "overwrite": false,
      "version": "0.9",
      "verbose": 2,
      "parameters": {
        "product": "MCD43A4",
        "version": "006",
        "serverurl": "http://e4ftl01.cr.usgs.gov"
      },
      "dstpath": {
        "volume": "None"
      }
    },
    {
      "processid": "searchDataPool",
      "overwrite": false,
      "version": "0.9",
      "verbose": 2,
      "parameters": {
        "product": "MYD09A1",
        "version": "006",
        "serverurl": "http://e4ftl01.cr.usgs.gov"
      },
      "dstpath": {
        "volume": "None"
      }
    },
    {
      "processid": "searchDataPool",
      "overwrite": false,
      "version": "0.9",
      "verbose": 2,
      "parameters": {
        "product": "MOD09A1",
        "version": "006",
        "serverurl": "http://e4ftl01.cr.usgs.gov"
      },
      "dstpath": {
        "volume": "None"
      }
    }
  ]
}
```
