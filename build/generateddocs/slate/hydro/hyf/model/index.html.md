---
title: HY_HydroFeature (Schema)

toc_footers:
  - Version 1.0
  - <a href='#'>HY_HydroFeature</a>
  - <a href='https://blocks.ogc.org/register.html'>Building Blocks register</a>

search: true

code_clipboard: true

meta:
  - name: HY_HydroFeature (Schema)
---


# HY_HydroFeature `ogc.hydro.hyf.model`

HY Features Core model

<p class="status">
    <span data-rainbow-uri="http://www.opengis.net/def/status">Status</span>:
    <a href="http://www.opengis.net/def/status/under-development" target="_blank" data-rainbow-uri>Under development</a>
</p>

<aside class="success">
This building block is <strong>valid</strong>
</aside>


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
            upperCatchment:
              type: array
              items:
                type: string
                format: uri
              uniqueItems: true
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

```

> <a target="_blank" href="https://avillar.github.io/TreedocViewer/?dataParser=yaml&amp;dataUrl=https%3A%2F%2Fogcincubator.github.io%2Fbblocks-hydro%2Fbuild%2Fannotated%2Fhydro%2Fhyf%2Fmodel%2Fschema.yaml&amp;expand=2&amp;option=%7B%22showTable%22%3A+false%7D">View on YAML Viewer</a>

Links to the schema:

* YAML version: <a href="https://ogcincubator.github.io/bblocks-hydro/build/annotated/hydro/hyf/model/schema.yaml" target="_blank">https://ogcincubator.github.io/bblocks-hydro/build/annotated/hydro/hyf/model/schema.yaml</a>
* JSON version: <a href="https://ogcincubator.github.io/bblocks-hydro/build/annotated/hydro/hyf/model/schema.json" target="_blank">https://ogcincubator.github.io/bblocks-hydro/build/annotated/hydro/hyf/model/schema.json</a>

# References

* [OGC API - Features, Part 1, 7.16.2: Feature Response](https://docs.ogc.org/is/17-069r3/17-069r3.html#_response_7)

# For developers

The source code for this Building Block can be found in the following repository:

* URL: <a href="https://github.com/ogcincubator/bblocks-hydro" target="_blank">https://github.com/ogcincubator/bblocks-hydro</a>
* Path:
<code><a href="https://github.com/ogcincubator/bblocks-hydro/blob/HEAD/_sources/model" target="_blank">_sources/model</a></code>

