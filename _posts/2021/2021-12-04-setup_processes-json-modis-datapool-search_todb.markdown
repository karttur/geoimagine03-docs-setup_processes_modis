---
layout: article
title: modis-datapool-search_todb_v090.json
categories: setup_processes
excerpt:  Add html search results to the db
tags:: 
    - json/modis-datapool-search_todb
date: 2021-12-04
modified: 2021-12-04
comments: true
share: true
---

# json/modis datapool search todb (setup_processes)

###  Add html search results to the db

The json command file <span class='file'>modis-datapool-search_todb_v090.json</span> is part of karttur's GeoImagine project <span class='project'>setup_processes</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

```
{
  "datapooldb": {
    "userproj": {
      "userid": "karttur",
      "projectid": "karttur",
      "tractid": "karttur",
      "siteid": "*",
      "plotid": "*",
      "system": "modis"
    },
    "period": {
      "startyear": "2000",
      "endyear": "2020",
      "timestep": "8D"
    },
    "process": [
      {
        "processid": "ModisSearchToDB",
        "dsversion": "1.3",
        "parameters": {
          "product": "MCD43A4",
          "version": "006"
        },
        "srcpath": {
          "volume": "None"
        }
      },
      {
        "processid": "ModisSearchToDB",
        "dsversion": "1.3",
        "parameters": {
          "product": "MYD09A1",
          "version": "006"
        },
        "srcpath": {
          "volume": "None"
        }
      },
      {
        "processid": "ModisSearchToDB",
        "dsversion": "1.3",
        "parameters": {
          "product": "MOD09A1",
          "version": "006"
        },
        "srcpath": {
          "volume": "None"
        }
      }
    ]
  }
}
```
