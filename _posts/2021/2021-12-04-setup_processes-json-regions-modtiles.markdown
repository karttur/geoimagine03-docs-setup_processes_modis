---
layout: article
title: regions-modtiles_v090.json
categories: setup_processes
excerpt:  Link default regions to MODIS SIN grid tiles
tags:: 
    - json/regions-modtiles
date: 2021-12-04
modified: 2021-12-04
comments: true
share: true
---

# json/regions modtiles (setup_processes)

###  Link default regions to MODIS SIN grid tiles

The json command file <span class='file'>regions-modtiles_v090.json</span> is part of karttur's GeoImagine project <span class='project'>setup_processes</span>. Calling the json file will execute the following commands of the GeoImagine Framework.

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
    "startyear": 2014,
    "endyear": 2014,
    "timestep": "singleyear"
  },
  "process": [
    {
      "processid": "LinkDefaultRegionTiles",
      "overwrite": false,
      "version": "0.9",
      "verbose": 2,
      "parameters": {
        "defregmask": "global",
        "regioncat": "continent",
        "onlyregionsfullywithinsystem": false
      },
      "srcpath": {
        "volume": "DEMDATA",
        "hdr": "shp",
        "dat": "shp"
      },
      "dstpath": {
        "volume": "DEMDATA"
      },
      "srccomp": [
        {
          "regions": {
            "source": "karttur",
            "product": "karttur",
            "content": "roi",
            "layerid": "defreg",
            "prefix": "defreg",
            "suffix": "tol@1km"
          }
        }
      ],
      "dstcomp": [
        {
          "region": {
            "source": "karttur",
            "product": "karttur",
            "content": "roi",
            "layerid": "defreg",
            "prefix": "defreg",
            "suffix": "tol@1km"
          }
        }
      ]
    },
    {
      "processid": "LinkDefaultRegionTiles",
      "overwrite": false,
      "version": "0.9",
      "verbose": 2,
      "parameters": {
        "defregmask": "global",
        "regioncat": "subcontinent",
        "onlyregionsfullywithinsystem": false
      },
      "srcpath": {
        "volume": "DEMDATA",
        "hdr": "shp",
        "dat": "shp"
      },
      "dstpath": {
        "volume": "DEMDATA"
      },
      "srccomp": [
        {
          "regions": {
            "source": "karttur",
            "product": "karttur",
            "content": "roi",
            "layerid": "defreg",
            "prefix": "defreg",
            "suffix": "tol@1km"
          }
        }
      ],
      "dstcomp": [
        {
          "region": {
            "source": "karttur",
            "product": "karttur",
            "content": "roi",
            "layerid": "defreg",
            "prefix": "defreg",
            "suffix": "tol@1km"
          }
        }
      ]
    },
    {
      "processid": "LinkDefaultRegionTiles",
      "overwrite": false,
      "version": "0.9",
      "verbose": 2,
      "parameters": {
        "defregmask": "global",
        "regioncat": "country",
        "onlyregionsfullywithinsystem": false
      },
      "srcpath": {
        "volume": "DEMDATA",
        "hdr": "shp",
        "dat": "shp"
      },
      "dstpath": {
        "volume": "DEMDATA"
      },
      "srccomp": [
        {
          "regions": {
            "source": "karttur",
            "product": "karttur",
            "content": "roi",
            "layerid": "defreg",
            "prefix": "defreg",
            "suffix": "tol@100m"
          }
        }
      ],
      "dstcomp": [
        {
          "region": {
            "source": "karttur",
            "product": "karttur",
            "content": "roi",
            "layerid": "defreg",
            "prefix": "defreg",
            "suffix": "tol@100m"
          }
        }
      ]
    },
    {
      "processid": "LinkDefaultRegionTiles",
      "overwrite": false,
      "version": "0.9",
      "verbose": 2,
      "parameters": {
        "defregmask": "global",
        "regioncat": "continentcountry",
        "onlyregionsfullywithinsystem": false
      },
      "srcpath": {
        "volume": "DEMDATA",
        "hdr": "shp",
        "dat": "shp"
      },
      "dstpath": {
        "volume": "DEMDATA"
      },
      "srccomp": [
        {
          "regions": {
            "source": "karttur",
            "product": "karttur",
            "content": "roi",
            "layerid": "defreg",
            "prefix": "defreg",
            "suffix": "tol@100m"
          }
        }
      ],
      "dstcomp": [
        {
          "region": {
            "source": "karttur",
            "product": "karttur",
            "content": "roi",
            "layerid": "defreg",
            "prefix": "defreg",
            "suffix": "tol@100m"
          }
        }
      ]
    },
    {
      "processid": "LinkDefaultRegionTiles",
      "overwrite": false,
      "version": "0.9",
      "verbose": 2,
      "parameters": {
        "defregmask": "global",
        "regioncat": "marinecontinent",
        "onlyregionsfullywithinsystem": false
      },
      "srcpath": {
        "volume": "DEMDATA",
        "hdr": "shp",
        "dat": "shp"
      },
      "dstpath": {
        "volume": "DEMDATA"
      },
      "srccomp": [
        {
          "regions": {
            "source": "karttur",
            "product": "karttur",
            "content": "roi",
            "layerid": "defreg",
            "prefix": "defreg",
            "suffix": "0"
          }
        }
      ],
      "dstcomp": [
        {
          "region": {
            "source": "karttur",
            "product": "karttur",
            "content": "roi",
            "layerid": "defreg",
            "prefix": "defreg",
            "suffix": "0"
          }
        }
      ]
    },
    {
      "processid": "LinkDefaultRegionTiles",
      "overwrite": false,
      "version": "0.9",
      "verbose": 2,
      "parameters": {
        "defregmask": "global",
        "regioncat": "marinesubcontinent",
        "onlyregionsfullywithinsystem": false
      },
      "srcpath": {
        "volume": "DEMDATA",
        "hdr": "shp",
        "dat": "shp"
      },
      "dstpath": {
        "volume": "DEMDATA"
      },
      "srccomp": [
        {
          "regions": {
            "source": "karttur",
            "product": "karttur",
            "content": "roi",
            "layerid": "defreg",
            "prefix": "defreg",
            "suffix": "0"
          }
        }
      ],
      "dstcomp": [
        {
          "region": {
            "source": "karttur",
            "product": "karttur",
            "content": "roi",
            "layerid": "defreg",
            "prefix": "defreg",
            "suffix": "0"
          }
        }
      ]
    },
    {
      "processid": "LinkDefaultRegionTiles",
      "overwrite": false,
      "version": "0.9",
      "verbose": 2,
      "parameters": {
        "defregmask": "global",
        "regioncat": "marinecountry",
        "onlyregionsfullywithinsystem": false
      },
      "srcpath": {
        "volume": "DEMDATA",
        "hdr": "shp",
        "dat": "shp"
      },
      "dstpath": {
        "volume": "DEMDATA"
      },
      "srccomp": [
        {
          "regions": {
            "source": "karttur",
            "product": "karttur",
            "content": "roi",
            "layerid": "defreg",
            "prefix": "defreg",
            "suffix": "0"
          }
        }
      ],
      "dstcomp": [
        {
          "region": {
            "source": "karttur",
            "product": "karttur",
            "content": "roi",
            "layerid": "defreg",
            "prefix": "defreg",
            "suffix": "0"
          }
        }
      ]
    },
    {
      "processid": "LinkDefaultRegionTiles",
      "overwrite": false,
      "version": "0.9",
      "verbose": 2,
      "parameters": {
        "defregmask": "global",
        "regioncat": "marinecontinentcountry",
        "onlyregionsfullywithinsystem": false
      },
      "srcpath": {
        "volume": "DEMDATA",
        "hdr": "shp",
        "dat": "shp"
      },
      "dstpath": {
        "volume": "DEMDATA"
      },
      "srccomp": [
        {
          "regions": {
            "source": "karttur",
            "product": "karttur",
            "content": "roi",
            "layerid": "defreg",
            "prefix": "defreg",
            "suffix": "0"
          }
        }
      ],
      "dstcomp": [
        {
          "region": {
            "source": "karttur",
            "product": "karttur",
            "content": "roi",
            "layerid": "defreg",
            "prefix": "defreg",
            "suffix": "0"
          }
        }
      ]
    },
    {
      "processid": "LinkDefaultRegionTiles",
      "overwrite": false,
      "version": "0.9",
      "verbose": 2,
      "parameters": {
        "defregmask": "global",
        "regioncat": "global",
        "onlyregionsfullywithinsystem": false
      },
      "srcpath": {
        "volume": "DEMDATA",
        "hdr": "shp",
        "dat": "shp"
      },
      "dstpath": {
        "volume": "DEMDATA"
      },
      "srccomp": [
        {
          "regions": {
            "source": "karttur",
            "product": "karttur",
            "content": "roi",
            "layerid": "defreg",
            "prefix": "defreg",
            "suffix": "0"
          }
        }
      ],
      "dstcomp": [
        {
          "region": {
            "source": "karttur",
            "product": "karttur",
            "content": "roi",
            "layerid": "defreg",
            "prefix": "defreg",
            "suffix": "0"
          }
        }
      ]
    }
  ]
}
```
