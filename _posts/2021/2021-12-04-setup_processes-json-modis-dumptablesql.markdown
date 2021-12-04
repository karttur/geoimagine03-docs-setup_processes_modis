---
layout: article
title: modis-dumptablesql_v090.json
categories: setup_processes
excerpt: \# dump (sql) and export (csv) the content of the db tables for MODIS tilecoords and regions
tags:: 
    - json/modis-dumptablesql
date: 2021-12-04
modified: 2021-12-04
comments: true
share: true
---

# json/modis dumptablesql (setup_processes)

### \# dump (sql) and export (csv) the content of the db tables for MODIS tilecoords and regions

The json command file <span class='file'>modis-dumptablesql_v090.json</span> is part of karttur's GeoImagine project <span class='project'>setup_processes</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

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
      "processid": "DumpTableSQL",
      "overwrite": true,
      "version": "0.9",
      "verbose": 2,
      "parameters": {
        "schema": "modis",
        "table": "tilecoords",
        "format": "c",
        "cmdpath": "/usr/local/bin",
        "dataonly": true,
        "definitiononly": false
      },
      "dstpath": {
        "volume": "DEMDATA"
      }
    },
    {
      "processid": "ExportTableCsv",
      "overwrite": true,
      "version": "0.9",
      "verbose": 2,
      "parameters": {
        "schema": "modis",
        "table": "tilecoords"
      },
      "dstpath": {
        "volume": "DEMDATA"
      }
    },
    {
      "processid": "DumpTableSQL",
      "overwrite": true,
      "version": "0.9",
      "verbose": 2,
      "parameters": {
        "schema": "modis",
        "table": "regions",
        "format": "c",
        "cmdpath": "/usr/local/bin",
        "dataonly": true,
        "definitiononly": false
      },
      "dstpath": {
        "volume": "DEMDATA"
      }
    },
    {
      "processid": "ExportTableCsv",
      "overwrite": true,
      "version": "0.9",
      "verbose": 2,
      "parameters": {
        "schema": "modis",
        "table": "regions"
      },
      "dstpath": {
        "volume": "DEMDATA"
      }
    }
  ]
}
```
