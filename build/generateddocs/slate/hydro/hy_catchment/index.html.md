---
title: HY_Basin (Schema)

language_tabs:
  - json: JSON
  - jsonld: JSON-LD

toc_footers:
  - Version 1.0
  - <a href='#'>HY_Basin</a>
  - <a href='https://blocks.ogc.org/register.html'>Building Blocks register</a>

search: true

code_clipboard: true

meta:
  - name: HY_Basin (Schema)
---


# HY_Basin `ogc.hydro.hy_catchment`

HY Feature example - HY_Basin

<p class="status">
    <span data-rainbow-uri="http://www.opengis.net/def/status">Status</span>:
    <a href="http://www.opengis.net/def/status/under-development" target="_blank" data-rainbow-uri>Under development</a>
</p>

<aside class="warning">
Validation for this building block has <strong><a href="https://github.com/ogcincubator/bblocks-hydro/blob/master/build/tests/hydro/hy_catchment/" target="_blank">failed</a></strong>
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
    <a target="_blank" href="https://ogcincubator.github.io/bblocks-hydro/build/tests/hydro/hy_catchment/example_1_1.json">Open in new window</a>
    <a target="_blank" href="https://avillar.github.io/TreedocViewer/?dataParser=json&amp;dataUrl=https%3A%2F%2Fogcincubator.github.io%2Fbblocks-hydro%2Fbuild%2Ftests%2Fhydro%2Fhy_catchment%2Fexample_1_1.json&amp;expand=2&amp;option=%7B%22showTable%22%3A+false%7D">View on JSON Viewer</a></p>
</blockquote>




```jsonld
{
  "type": "Feature",
  "featureType": "HY_Basin",
  "properties": {
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
  "@context": "https://ogcincubator.github.io/bblocks-hydro/build/annotated/hydro/hy_catchment/context.jsonld"
}
```

<blockquote class="lang-specific jsonld">
  <p class="example-links">
    <a target="_blank" href="https://ogcincubator.github.io/bblocks-hydro/build/tests/hydro/hy_catchment/example_1_1.jsonld">Open in new window</a>
    <a target="_blank" href="https://json-ld.org/playground/#json-ld=https%3A%2F%2Fogcincubator.github.io%2Fbblocks-hydro%2Fbuild%2Ftests%2Fhydro%2Fhy_catchment%2Fexample_1_1.jsonld">View on JSON-LD Playground</a>
</blockquote>




# JSON Schema

```yaml--schema
$schema: https://json-schema.org/draft/2019-09/schema
$id: https://www.opengis.net/def/schema/hy_features/hyf/HY_HydroFeature.json
$defs:
  HY_Basin:
    $anchor: HY_Basin
    allOf:
    - $ref: '#/$defs/HY_Catchment'
    - type: object
      properties:
        properties:
          type: object
          properties:
            upstreamBasin:
              type: array
              items:
                type: string
                format: uri
              uniqueItems: true
              x-jsonld-type: '@id'
              x-jsonld-id: https://www.opengis.net/def/schema/hy_features/hyf/HY_HydroFeature/hya/HY_HydroFeature/upstreamBasin
            code:
              type: string
            inflowNode:
              type: string
              format: uri
            outflowNode:
              type: string
              format: uri
          required:
          - outflowNode
      required:
      - properties
  HY_BasinAggregate:
    $anchor: HY_BasinAggregate
    allOf:
    - $ref: '#/$defs/HY_Catchment'
    - type: object
      properties:
        properties:
          type: object
          properties:
            subBasin:
              type: array
              minItems: 1
              items:
                type: string
                format: uri
              uniqueItems: true
          required:
          - subBasin
      required:
      - properties
  HY_Catchment:
    $anchor: HY_Catchment
    allOf:
    - $ref: '#/$defs/HY_HydroFeature'
    - type: object
      properties:
        properties:
          type: object
          properties:
            containingCatchment:
              type: string
              format: uri
  HY_CatchmentArea:
    $anchor: HY_CatchmentArea
    allOf:
    - $ref: '#/$defs/HY_CatchmentRepresentation'
    - type: object
  HY_CatchmentBoundary:
    $anchor: HY_CatchmentBoundary
    allOf:
    - $ref: '#/$defs/HY_CatchmentRepresentation'
    - type: object
  HY_CatchmentRepresentation:
    $anchor: HY_CatchmentRepresentation
    type: object
    properties:
      properties:
        type: object
        properties:
          '@type':
            type: string
          representedCatchment:
            type: string
            format: uri
        required:
        - '@type'
        - representedCatchment
    required:
    - properties
  HY_CrossSection:
    $anchor: HY_CrossSection
    type: object
    properties:
      properties:
        type: object
        properties:
          '@type':
            type: string
          upstreamCrossSection:
            type: array
            items:
              type: string
              format: uri
            uniqueItems: true
          crossSectionPoint:
            type: array
            items:
              type: string
              format: uri
            uniqueItems: true
        required:
        - '@type'
    required:
    - properties
  HY_DistanceToRefPoint:
    $anchor: HY_DistanceToRefPoint
    type: object
    properties:
      properties:
        type: object
        properties:
          '@type':
            type: string
          distanceValue:
            type: number
          accuracyStatement:
            type: number
          precisionStatement:
            type: number
        required:
        - '@type'
        - distanceValue
    required:
    - properties
  HY_FlowPath:
    $anchor: HY_FlowPath
    allOf:
    - $ref: '#/$defs/HY_CatchmentRepresentation'
    - type: object
  HY_Glacier:
    $anchor: HY_Glacier
    allOf:
    - $ref: '#/$defs/HY_HydroFeature'
    - type: object
  HY_HydroFeature:
    $anchor: HY_HydroFeature
    type: object
    properties:
      properties:
        type: object
        properties:
          '@type':
            type: string
          identifier:
            type: array
            items:
              type: string
            uniqueItems: true
          name:
            type: array
            items:
              $ref: '#/$defs/HY_HydroFeatureName'
            uniqueItems: true
          context:
            type: array
            items:
              $ref: '#/$defs/HY_HydroFeatureContext'
            uniqueItems: true
        required:
        - '@type'
    required:
    - properties
  HY_HydroFeatureContext:
    $anchor: HY_HydroFeatureContext
    type: object
    properties:
      '@type':
        type: string
      hydroFeature:
        type: string
        format: uri
      classification:
        type: array
        items:
          type: string
        uniqueItems: true
      spatialContext:
        type: array
        items:
          type: string
        uniqueItems: true
      temporalContext:
        type: array
        items:
          type: string
        uniqueItems: true
    required:
    - '@type'
  HY_HydroFeatureName:
    $anchor: HY_HydroFeatureName
    type: string
  HY_HydrographicNetwork:
    $anchor: HY_HydrographicNetwork
    allOf:
    - $ref: '#/$defs/HY_Network'
    - type: object
  HY_IndirectPosition:
    $anchor: HY_IndirectPosition
    type: object
    properties:
      properties:
        type: object
        properties:
          '@type':
            type: string
          distanceToRefPoint:
            type: string
            format: uri
          relativePosition:
            type: string
            format: uri
          referencePoint:
            type: array
            minItems: 1
            items:
              type: string
              format: uri
            uniqueItems: true
          mileageCS:
            type: string
            format: uri
        required:
        - '@type'
        - referencePoint
    required:
    - properties
  HY_LongitudinalSection:
    $anchor: HY_LongitudinalSection
    type: object
    properties:
      properties:
        type: object
        properties:
          '@type':
            type: string
          longitudinalSectionPoint:
            type: array
            items:
              type: string
              format: uri
            uniqueItems: true
        required:
        - '@type'
    required:
    - properties
  HY_MileageSystemAxis:
    $anchor: HY_MileageSystemAxis
    type: object
    properties:
      properties:
        type: object
        properties:
          '@type':
            type: string
          precision:
            type: number
        required:
        - '@type'
    required:
    - properties
  HY_Network:
    $anchor: HY_Network
    allOf:
    - $ref: '#/$defs/HY_CatchmentRepresentation'
    - type: object
  HY_Outfall:
    $anchor: HY_Outfall
    type: object
    properties:
      properties:
        type: object
        properties:
          '@type':
            type: string
          receivingBasin:
            type: array
            items:
              type: string
              format: uri
            uniqueItems: true
          contributingBasin:
            type: array
            minItems: 1
            items:
              type: string
              format: uri
            uniqueItems: true
          position:
            type: string
            format: uri
        required:
        - '@type'
        - contributingBasin
        - position
    required:
    - properties
  HY_RefPointType:
    $anchor: HY_RefPointType
    type: string
    format: uri
  HY_ReferencePoint:
    $anchor: HY_ReferencePoint
    type: object
    properties:
      geometry:
        $ref: https://geojson.org/schema/Point.json
      properties:
        type: object
        properties:
          '@type':
            type: string
          refPointType:
            $ref: '#/$defs/HY_RefPointType'
          networkLocation:
            type: string
            format: uri
        required:
        - '@type'
    required:
    - properties
  HY_RelativePosition:
    $anchor: HY_RelativePosition
    type: object
    properties:
      properties:
        type: object
        properties:
          '@type':
            type: string
          description:
            $ref: '#/$defs/HY_RelativePositionDescription'
          percentage:
            type: number
        required:
        - '@type'
    required:
    - properties
  HY_RelativePositionDescription:
    $anchor: HY_RelativePositionDescription
    type: string
    format: uri
  HY_Reservoir:
    $anchor: HY_Reservoir
    allOf:
    - $ref: '#/$defs/HY_HydroFeature'
    - type: object
  HY_RiverMileageCS:
    $anchor: HY_RiverMileageCS
    type: object
    properties:
      properties:
        type: object
        properties:
          '@type':
            type: string
          axis:
            type: array
            minItems: 1
            items:
              type: string
              format: uri
            uniqueItems: true
        required:
        - '@type'
        - axis
    required:
    - properties
  HY_WaterBody:
    $anchor: HY_WaterBody
    allOf:
    - $ref: '#/$defs/HY_HydroFeature'
    - type: object
      properties:
        properties:
          type: object
          properties:
            hydrographicNetwork:
              type: string
              format: uri
          required:
          - hydrographicNetwork
      required:
      - properties
  HY_WaterBodySegment:
    $anchor: HY_WaterBodySegment
    allOf:
    - $ref: '#/$defs/HY_HydroFeature'
    - type: object
      properties:
        properties:
          type: object
          properties:
            streamCrossSection:
              type: array
              items:
                type: string
                format: uri
              uniqueItems: true
            streamLongitudinalSection:
              type: array
              items:
                type: string
                format: uri
              uniqueItems: true
            upstreamSegment:
              type: array
              items:
                type: string
                format: uri
              uniqueItems: true
            downstreamSegment:
              type: array
              items:
                type: string
                format: uri
              uniqueItems: true
            waterBody:
              type: string
              format: uri
            fixedLandmark:
              type: array
              items:
                type: string
                format: uri
              uniqueItems: true
          required:
          - waterBody
      required:
      - properties
  HY_WaterBodyStratum:
    $anchor: HY_WaterBodyStratum
    type: object
    properties:
      properties:
        type: object
        properties:
          '@type':
            type: string
          stratumType:
            type: array
            items:
              type: string
            uniqueItems: true
          segment:
            type: string
            format: uri
          storage:
            type: array
            items:
              type: string
              format: uri
            uniqueItems: true
        required:
        - '@type'
        - segment
    required:
    - properties
  HY_Water_LiquidPhase:
    $anchor: HY_Water_LiquidPhase
    type: object
    properties:
      properties:
        type: object
        properties:
          '@type':
            type: string
          accumulatingWaterBody:
            type: array
            items:
              type: string
              format: uri
            uniqueItems: true
        required:
        - '@type'
    required:
    - properties
  HY_Water_SolidPhase:
    $anchor: HY_Water_SolidPhase
    type: object
    properties:
      properties:
        type: object
        properties:
          '@type':
            type: string
          coveredWaterBody:
            type: array
            items:
              type: string
              format: uri
            uniqueItems: true
          snowmelt:
            type: string
            format: uri
          accumulatingGlacier:
            type: array
            items:
              type: string
              format: uri
            uniqueItems: true
        required:
        - '@type'
    required:
    - properties
  HY_Watershed:
    $anchor: HY_Watershed
    allOf:
    - $ref: '#/$defs/HY_CatchmentBoundary'
    - type: object
      properties:
        properties:
          type: object
          properties:
            outfall:
              type: string
              format: uri
x-jsonld-extra-terms:
  prev:
    x-jsonld-type: '@id'
    x-jsonld-id: https://www.opengis.net/def/schema/hy_features/hyf/HY_HydroFeature/hya/HY_HydroFeature/upstreamBasin
  hyf:upstreamBasin:
    x-jsonld-type: '@id'
    x-jsonld-id: https://www.opengis.net/def/schema/hy_features/hyf/HY_HydroFeature/hya/HY_HydroFeature/upstreamBasin
x-jsonld-prefixes:
  hyf: https://www.opengis.net/def/schema/hy_features/hyf/HY_HydroFeature/hya/HY_HydroFeature/

```

> <a target="_blank" href="https://avillar.github.io/TreedocViewer/?dataParser=yaml&amp;dataUrl=https%3A%2F%2Fogcincubator.github.io%2Fbblocks-hydro%2Fbuild%2Fannotated%2Fhydro%2Fhy_catchment%2Fschema.yaml&amp;expand=2&amp;option=%7B%22showTable%22%3A+false%7D">View on YAML Viewer</a>

Links to the schema:

* YAML version: <a href="https://ogcincubator.github.io/bblocks-hydro/build/annotated/hydro/hy_catchment/schema.yaml" target="_blank">https://ogcincubator.github.io/bblocks-hydro/build/annotated/hydro/hy_catchment/schema.yaml</a>
* JSON version: <a href="https://ogcincubator.github.io/bblocks-hydro/build/annotated/hydro/hy_catchment/schema.json" target="_blank">https://ogcincubator.github.io/bblocks-hydro/build/annotated/hydro/hy_catchment/schema.json</a>


# JSON-LD Context

```json--ldContext
{
  "@context": {
    "prev": {
      "@type": "@id",
      "@id": "hyf:upstreamBasin"
    },
    "hyf:upstreamBasin": {
      "@type": "@id",
      "@id": "hyf:upstreamBasin"
    },
    "hyf": "https://www.opengis.net/def/schema/hy_features/hyf/HY_HydroFeature/hya/HY_HydroFeature/",
    "@version": 1.1
  }
}
```

> <a target="_blank" href="https://json-ld.org/playground/#json-ld=https%3A%2F%2Fogcincubator.github.io%2Fbblocks-hydro%2Fbuild%2Fannotated%2Fhydro%2Fhy_catchment%2Fcontext.jsonld">View on JSON-LD Playground</a>

You can find the full JSON-LD context here:
<a href="https://ogcincubator.github.io/bblocks-hydro/build/annotated/hydro/hy_catchment/context.jsonld" target="_blank">https://ogcincubator.github.io/bblocks-hydro/build/annotated/hydro/hy_catchment/context.jsonld</a>

# References

* [OGC API - Features, Part 1, 7.16.2: Feature Response](https://docs.ogc.org/is/17-069r3/17-069r3.html#_response_7)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: <a href="https://github.com/ogcincubator/bblocks-hydro" target="_blank">https://github.com/ogcincubator/bblocks-hydro</a>
* Path:
<code><a href="https://github.com/ogcincubator/bblocks-hydro/blob/HEAD/_sources/hy_catchment" target="_blank">_sources/hy_catchment</a></code>

