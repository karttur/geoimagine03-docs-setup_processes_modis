---
layout: article
title: modis-dumpschemasql_v090.json
categories: setup_processes
excerpt: \# dump (sql) and export (csv) the content of the db schema for MODIS
tags:: 
    - json/modis-dumpschemasql
date: 2021-12-04
modified: 2021-12-04
comments: true
share: true
---

# json/modis dumpschemasql (setup_processes)

### \# dump (sql) and export (csv) the content of the db schema for MODIS

The json command file <span class='file'>modis-dumpschemasql_v090.json</span> is part of karttur's GeoImagine project <span class='project'>setup_processes</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

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
      "processid": "DumpSchemaSQL",
      "overwrite": true,
      "version": "0.9",
      "verbose": 2,
      "parameters": {
        "schema": "modis",
        "format": "c",
        "cmdpath": "None",
        "dataonly": true,
        "definitiononly": false,
        "cmdpath": "/usr/local/bin"
      },
      "dstpath": {
        "volume": "DEMDATA"
      }
    },
    {
      "processid": "DumpSchemaSQL",
      "overwrite": true,
      "version": "0.9",
      "verbose": 2,
      "parameters": {
        "schema": "modis",
        "format": "p",
        "cmdpath": "None",
        "dataonly": true,
        "definitiononly": false,
        "cmdpath": "/usr/local/bin"
      },
      "dstpath": {
        "volume": "DEMDATA"
      }
    },
    {
      "processid": "ExportSchemaCsv",
      "overwrite": true,
      "version": "0.9",
      "verbose": 2,
      "parameters": {
        "schema": "modis"
      },
      "dstpath": {
        "volume": "DEMDATA"
      }
    }
  ]
}
```
