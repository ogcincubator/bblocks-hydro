---
title: HY_Basin (Schema)

language_tabs:
  - json: JSON
  - jsonld: JSON-LD
  - turtle: RDF/Turtle

toc_footers:
  - Version 1.0
  - <a href='#'>HY_Basin</a>
  - <a href='https://blocks.ogc.org/register.html'>Building Blocks register</a>

search: true

code_clipboard: true

meta:
  - name: HY_Basin (Schema)
---


# HY_Basin `ogc.hydro.hyf.classes.hy_catchment`

HY Feature example - HY_Basin

<p class="status">
    <span data-rainbow-uri="http://www.opengis.net/def/status">Status</span>:
    <a href="http://www.opengis.net/def/status/under-development" target="_blank" data-rainbow-uri>Under development</a>
</p>

<aside class="warning">
Validation for this building block has <strong><a href="https://github.com/ogcincubator/bblocks-hydro/blob/master/build/tests/hydro/hyf/classes/hy_catchment/" target="_blank">failed</a></strong>
</aside>

# Description

## HY_Basin

 A Building Block for a typical Class - HY_Basin

The schema is derived directly from the UML model, and it linked to an ontology also derived from the UML model.

The model schema is wrapped in a FG-JSON feature schema.



# Examples

## GeoJSON - specialisation example.



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
    "type": "MultiPolygon",
    "coordinates": [
      [
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

<blockquote class="lang-specific json">
  <p class="example-links">
    <a target="_blank" href="https://ogcincubator.github.io/bblocks-hydro/build/tests/hydro/hyf/classes/hy_catchment/example_1_1.json">Open in new window</a>
    <a target="_blank" href="https://avillar.github.io/TreedocViewer/?dataParser=json&amp;dataUrl=https%3A%2F%2Fogcincubator.github.io%2Fbblocks-hydro%2Fbuild%2Ftests%2Fhydro%2Fhyf%2Fclasses%2Fhy_catchment%2Fexample_1_1.json&amp;expand=2&amp;option=%7B%22showTable%22%3A+false%7D">View on JSON Viewer</a></p>
</blockquote>




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
    "type": "MultiPolygon",
    "coordinates": [
      [
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

<blockquote class="lang-specific jsonld">
  <p class="example-links">
    <a target="_blank" href="https://ogcincubator.github.io/bblocks-hydro/build/tests/hydro/hyf/classes/hy_catchment/example_1_1.jsonld">Open in new window</a>
    <a target="_blank" href="https://json-ld.org/playground/#json-ld=https%3A%2F%2Fogcincubator.github.io%2Fbblocks-hydro%2Fbuild%2Ftests%2Fhydro%2Fhyf%2Fclasses%2Fhy_catchment%2Fexample_1_1.jsonld">View on JSON-LD Playground</a>
</blockquote>




```turtle
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
    rdfs:seeAlso [ dcterms:type "application/json" ;
            ns1:relation <http://www.iana.org/assignments/relation/prev> ;
            oa:hasTarget <https://reference.geoconnex.us/collections/hu02/items/02?f=json> ],
        [ rdfs:label "HU02" ;
            dcterms:type "application/json" ;
            ns1:relation <http://www.iana.org/assignments/relation/collection> ;
            oa:hasTarget <https://reference.geoconnex.us/collections/hu02> ],
        [ rdfs:label "This document as HTML" ;
            dcterms:type "text/html" ;
            ns1:relation <http://www.iana.org/assignments/relation/alternate> ;
            oa:hasTarget <https://geoconnex.us/ref/hu02/03?f=html> ] ;
    geojson:geometry [ a geojson:MultiPolygon ;
            geojson:coordinates ( ( ( -8.279193e+01 2.469972e+01 ) ( -8.275341e+01 2.466845e+01 ) ( -8.275066e+01 2.465974e+01 ) ( -8.279193e+01 2.469972e+01 ) ) ) ] ;
    hyf:upstreamBasin <http://example.com/features/02> .


```

<blockquote class="lang-specific turtle">
  <p class="example-links">
    <a target="_blank" href="https://ogcincubator.github.io/bblocks-hydro/build/tests/hydro/hyf/classes/hy_catchment/example_1_1.ttl">Open in new window</a>
</blockquote>



## Basin as node point.



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
    "next": "04",
    "outflow": "03outflow"
  },
  "id": "03",
  "geometry": {
    "type": "Point",
    "coordinates":
        [
          -82.79192551924065,
          24.699718894664848
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

<blockquote class="lang-specific json">
  <p class="example-links">
    <a target="_blank" href="https://ogcincubator.github.io/bblocks-hydro/build/tests/hydro/hyf/classes/hy_catchment/example_2_1.json">Open in new window</a>
    <a target="_blank" href="https://avillar.github.io/TreedocViewer/?dataParser=json&amp;dataUrl=https%3A%2F%2Fogcincubator.github.io%2Fbblocks-hydro%2Fbuild%2Ftests%2Fhydro%2Fhyf%2Fclasses%2Fhy_catchment%2Fexample_2_1.json&amp;expand=2&amp;option=%7B%22showTable%22%3A+false%7D">View on JSON Viewer</a></p>
</blockquote>




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
    "next": "04",
    "outflow": "03outflow"
  },
  "id": "03",
  "geometry": {
    "type": "Point",
    "coordinates": [
      -82.79192551924065,
      24.699718894664848
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

<blockquote class="lang-specific jsonld">
  <p class="example-links">
    <a target="_blank" href="https://ogcincubator.github.io/bblocks-hydro/build/tests/hydro/hyf/classes/hy_catchment/example_2_1.jsonld">Open in new window</a>
    <a target="_blank" href="https://json-ld.org/playground/#json-ld=https%3A%2F%2Fogcincubator.github.io%2Fbblocks-hydro%2Fbuild%2Ftests%2Fhydro%2Fhyf%2Fclasses%2Fhy_catchment%2Fexample_2_1.jsonld">View on JSON-LD Playground</a>
</blockquote>




```turtle
@prefix dct: <http://purl.org/dc/terms/> .
@prefix geojson: <https://purl.org/geojson/vocab#> .
@prefix hyf: <https://www.opengis.net/def/schema/hy_features/hyf/HY_HydroFeature/hya/HY_HydroFeature/> .
@prefix ns1: <http://www.iana.org/assignments/> .
@prefix oa: <http://www.w3.org/ns/oa#> .
@prefix rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#> .
@prefix rdfs: <http://www.w3.org/2000/01/rdf-schema#> .
@prefix xsd: <http://www.w3.org/2001/XMLSchema#> .

<file:///github/workspace/03> a geojson:Feature,
        hyf:HY_Basin ;
    rdfs:seeAlso [ dct:type "application/json" ;
            ns1:relation <http://www.iana.org/assignments/relation/prev> ;
            oa:hasTarget <https://reference.geoconnex.us/collections/hu02/items/02?f=json> ],
        [ rdfs:label "This document as HTML" ;
            dct:type "text/html" ;
            ns1:relation <http://www.iana.org/assignments/relation/alternate> ;
            oa:hasTarget <https://geoconnex.us/ref/hu02/03?f=html> ],
        [ rdfs:label "HU02" ;
            dct:type "application/json" ;
            ns1:relation <http://www.iana.org/assignments/relation/collection> ;
            oa:hasTarget <https://reference.geoconnex.us/collections/hu02> ] ;
    geojson:geometry [ a geojson:Point ;
            geojson:coordinates ( -8.279193e+01 2.469972e+01 ) ] ;
    hyf:upstreamBasin <file:///github/workspace/02> .


```

<blockquote class="lang-specific turtle">
  <p class="example-links">
    <a target="_blank" href="https://ogcincubator.github.io/bblocks-hydro/build/tests/hydro/hyf/classes/hy_catchment/example_2_1.ttl">Open in new window</a>
</blockquote>



# JSON Schema

```yaml--schema
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

> <a target="_blank" href="https://avillar.github.io/TreedocViewer/?dataParser=yaml&amp;dataUrl=https%3A%2F%2Fogcincubator.github.io%2Fbblocks-hydro%2Fbuild%2Fannotated%2Fhydro%2Fhyf%2Fclasses%2Fhy_catchment%2Fschema.yaml&amp;expand=2&amp;option=%7B%22showTable%22%3A+false%7D">View on YAML Viewer</a>

Links to the schema:

* YAML version: <a href="https://ogcincubator.github.io/bblocks-hydro/build/annotated/hydro/hyf/classes/hy_catchment/schema.yaml" target="_blank">https://ogcincubator.github.io/bblocks-hydro/build/annotated/hydro/hyf/classes/hy_catchment/schema.yaml</a>
* JSON version: <a href="https://ogcincubator.github.io/bblocks-hydro/build/annotated/hydro/hyf/classes/hy_catchment/schema.json" target="_blank">https://ogcincubator.github.io/bblocks-hydro/build/annotated/hydro/hyf/classes/hy_catchment/schema.json</a>


# JSON-LD Context

```json--ldContext
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

> <a target="_blank" href="https://json-ld.org/playground/#json-ld=https%3A%2F%2Fogcincubator.github.io%2Fbblocks-hydro%2Fbuild%2Fannotated%2Fhydro%2Fhyf%2Fclasses%2Fhy_catchment%2Fcontext.jsonld">View on JSON-LD Playground</a>

You can find the full JSON-LD context here:
<a href="https://ogcincubator.github.io/bblocks-hydro/build/annotated/hydro/hyf/classes/hy_catchment/context.jsonld" target="_blank">https://ogcincubator.github.io/bblocks-hydro/build/annotated/hydro/hyf/classes/hy_catchment/context.jsonld</a>

# References

* [OGC API - Features, Part 1, 7.16.2: Feature Response](https://docs.ogc.org/is/17-069r3/17-069r3.html#_response_7)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: <a href="https://github.com/ogcincubator/bblocks-hydro" target="_blank">https://github.com/ogcincubator/bblocks-hydro</a>
* Path:
<code><a href="https://github.com/ogcincubator/bblocks-hydro/blob/HEAD/_sources/classes/hy_catchment" target="_blank">_sources/classes/hy_catchment</a></code>

