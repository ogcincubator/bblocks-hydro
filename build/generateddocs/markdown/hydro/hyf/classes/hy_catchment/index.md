
# HY_Basin (Schema)

`ogc.hydro.hyf.classes.hy_catchment` *v1.0*

HY Feature example - HY_Basin

[*Status*](http://www.opengis.net/def/status): Under development

## Description

## HY_Basin

 A Building Block for a typical Class - HY_Basin

The schema is derived directly from the UML model, and it linked to an ontology also derived from the UML model.

The model schema is wrapped in a FG-JSON feature schema.



## Examples

### GeoJSON - specialisation example.
#### json
```json
{
  "type": "Feature",

  "featureType": "HY_Basin",
  "properties": {
      "@type": "hyf:HY_Basin",
    "gnis_url": "https://geonames.usgs.gov/apex/f?p=gnispq:3:::NO::P3_FID:2730133",
    "uri": "https://geoconnex.us/ref/hu02/03",
    "gnis_id": 2730133,
    "name": "South Atlantic-Gulf Region",
    "fid": 15,
    "loaddate": "2018-07-17T15:44:28+00:00",
    "prev": "02",
    "next": "04"
  },
  "id": "03",
  "geometry": {
    "type": "Polygon",
    "coordinates": [

        [
          -82.79192551924065,
          24.699718894664848
        ],
        [
          -82.75341358941488,
          24.668448982060728
        ],
        [
          -82.75066457497482,
          24.65974178394976
        ],
        [
          -82.79192551924065,
          24.699718894664848
        ]
      
    ]

  },
  "links": [

    {
      "rel": "alternate",
      "type": "text/html",
      "title": "This document as HTML",
      "href": "https://geoconnex.us/ref/hu02/03?f=html"
    },
    {
      "rel": "collection",
      "type": "application/json",
      "title": "HU02",
      "href": "https://reference.geoconnex.us/collections/hu02"
    },
    {
      "rel": "prev",
      "type": "application/json",
      "href": "https://reference.geoconnex.us/collections/hu02/items/02?f=json"
    }
  ]
}

```

#### jsonld
```jsonld
{
  "type": "Feature",
  "featureType": "HY_Basin",
  "properties": {
    "@type": "hyf:HY_Basin",
    "gnis_url": "https://geonames.usgs.gov/apex/f?p=gnispq:3:::NO::P3_FID:2730133",
    "uri": "https://geoconnex.us/ref/hu02/03",
    "gnis_id": 2730133,
    "name": "South Atlantic-Gulf Region",
    "fid": 15,
    "loaddate": "2018-07-17T15:44:28+00:00",
    "prev": "02",
    "next": "04"
  },
  "id": "03",
  "geometry": {
    "type": "Polygon",
    "coordinates": [
      [
        -82.79192551924065,
        24.699718894664848
      ],
      [
        -82.75341358941488,
        24.668448982060728
      ],
      [
        -82.75066457497482,
        24.65974178394976
      ],
      [
        -82.79192551924065,
        24.699718894664848
      ]
    ]
  },
  "links": [
    {
      "rel": "alternate",
      "type": "text/html",
      "title": "This document as HTML",
      "href": "https://geoconnex.us/ref/hu02/03?f=html"
    },
    {
      "rel": "collection",
      "type": "application/json",
      "title": "HU02",
      "href": "https://reference.geoconnex.us/collections/hu02"
    },
    {
      "rel": "prev",
      "type": "application/json",
      "href": "https://reference.geoconnex.us/collections/hu02/items/02?f=json"
    }
  ],
  "@context": "https://ogcincubator.github.io/bblocks-hydro/build/annotated/hydro/hyf/classes/hy_catchment/context.jsonld"
}
```

#### ttl
```ttl
@prefix dcterms: <http://purl.org/dc/terms/> .
@prefix geojson: <https://purl.org/geojson/vocab#> .
@prefix hyf: <https://www.opengis.net/def/schema/hy_features/hyf/HY_HydroFeature/hya/HY_HydroFeature/> .
@prefix ns1: <http://www.iana.org/assignments/> .
@prefix oa: <http://www.w3.org/ns/oa#> .
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

<http://example.com/features/03> a geojson:Feature,
        hyf:HY_Basin ;
    rdfs:seeAlso [ rdfs:label "HU02" ;
            dcterms:type "application/json" ;
            ns1:relation <http://www.iana.org/assignments/relation/collection> ;
            oa:hasTarget <https://reference.geoconnex.us/collections/hu02> ],
        [ rdfs:label "This document as HTML" ;
            dcterms:type "text/html" ;
            ns1:relation <http://www.iana.org/assignments/relation/alternate> ;
            oa:hasTarget <https://geoconnex.us/ref/hu02/03?f=html> ],
        [ dcterms:type "application/json" ;
            ns1:relation <http://www.iana.org/assignments/relation/prev> ;
            oa:hasTarget <https://reference.geoconnex.us/collections/hu02/items/02?f=json> ] ;
    geojson:geometry [ a geojson:Polygon ;
            geojson:coordinates ( ( -8.279193e+01 2.469972e+01 ) ( -8.275341e+01 2.466845e+01 ) ( -8.275066e+01 2.465974e+01 ) ( -8.279193e+01 2.469972e+01 ) ) ] ;
    hyf:upstreamBasin <http://example.com/features/02> .


```

## Schema

```yaml
$schema: https://json-schema.org/draft/2020-12/schema
description: HY_Basin Feature
allOf:
- $ref: https://ogcincubator.github.io/bblocks-hydro/build/annotated/hydro/hyf/model/schema.yaml#/$defs/HY_Basin
- $ref: https://opengeospatial.github.io/bblocks/annotated-schemas/geo/features/feature/schema.yaml
x-jsonld-extra-terms:
  prev:
    x-jsonld-type: '@id'
    x-jsonld-id: https://www.opengis.net/def/schema/hy_features/hyf/HY_HydroFeature/hya/HY_HydroFeature/upstreamBasin
  upstreamBasin:
    x-jsonld-type: '@id'
    x-jsonld-id: https://www.opengis.net/def/schema/hy_features/hyf/HY_HydroFeature/hya/HY_HydroFeature/upstreamBasin
  hyf:upstreamBasin:
    x-jsonld-type: '@id'
    x-jsonld-id: https://www.opengis.net/def/schema/hy_features/hyf/HY_HydroFeature/hya/HY_HydroFeature/upstreamBasin
x-jsonld-prefixes:
  hyf: https://www.opengis.net/def/schema/hy_features/hyf/HY_HydroFeature/hya/HY_HydroFeature/

```

Links to the schema:

* YAML version: [schema.yaml](https://ogcincubator.github.io/bblocks-hydro/build/annotated/hydro/hyf/classes/hy_catchment/schema.json)
* JSON version: [schema.json](https://ogcincubator.github.io/bblocks-hydro/build/annotated/hydro/hyf/classes/hy_catchment/schema.yaml)


# JSON-LD Context

```jsonld
{
  "@context": {
    "type": "@type",
    "id": "@id",
    "properties": "@nest",
    "geometry": {
      "@context": {
        "coordinates": {
          "@container": "@list",
          "@id": "geojson:coordinates"
        }
      },
      "@id": "geojson:geometry"
    },
    "bbox": {
      "@container": "@list",
      "@id": "geojson:bbox"
    },
    "Feature": "geojson:Feature",
    "FeatureCollection": "geojson:FeatureCollection",
    "GeometryCollection": "geojson:GeometryCollection",
    "LineString": "geojson:LineString",
    "MultiLineString": "geojson:MultiLineString",
    "MultiPoint": "geojson:MultiPoint",
    "MultiPolygon": "geojson:MultiPolygon",
    "Point": "geojson:Point",
    "Polygon": "geojson:Polygon",
    "features": {
      "@container": "@set",
      "@id": "geojson:features"
    },
    "links": {
      "@context": {
        "href": {
          "@type": "@id",
          "@id": "oa:hasTarget"
        },
        "rel": {
          "@context": {
            "@base": "http://www.iana.org/assignments/relation/"
          },
          "@id": "http://www.iana.org/assignments/relation",
          "@type": "@id"
        },
        "type": "dct:type",
        "hreflang": "dct:language",
        "title": "rdfs:label",
        "length": "dct:extent"
      },
      "@id": "rdfs:seeAlso"
    },
    "prev": {
      "@type": "@id",
      "@id": "hyf:upstreamBasin"
    },
    "upstreamBasin": {
      "@type": "@id",
      "@id": "hyf:upstreamBasin"
    },
    "hyf:upstreamBasin": {
      "@type": "@id",
      "@id": "hyf:upstreamBasin"
    },
    "hyf": "https://www.opengis.net/def/schema/hy_features/hyf/HY_HydroFeature/hya/HY_HydroFeature/",
    "geojson": "https://purl.org/geojson/vocab#",
    "rdfs": "http://www.w3.org/2000/01/rdf-schema#",
    "oa": "http://www.w3.org/ns/oa#",
    "dct": "http://purl.org/dc/terms/",
    "@version": 1.1
  }
}
```

You can find the full JSON-LD context here:
[context.jsonld](https://ogcincubator.github.io/bblocks-hydro/build/annotated/hydro/hyf/classes/hy_catchment/context.jsonld)

## Sources

* [OGC API - Features, Part 1, 7.16.2: Feature Response](https://docs.ogc.org/is/17-069r3/17-069r3.html#_response_7)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: [https://github.com/ogcincubator/bblocks-hydro](https://github.com/ogcincubator/bblocks-hydro)
* Path: `_sources/classes/hy_catchment`

