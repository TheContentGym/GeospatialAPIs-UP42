# 4.Configure and Run The Job

A job is a unique instance of a pre-configured workflow that delivers the outputs defined by the JSON parameters in the job configuration. In this use case, we have the UP42_challenge.geojson file that defines this configuration. 

This topic includes information on creating and job and running it. You can also rerun a job created earlier. For more information on rerunning a job created earlier, see [Rerun A Job](Specify-the-area-and-run-the-job.md).

## UP42_challenge.geojson
In this guide, we are using the UP42_challenge.geojson file, which specifies the coordinates of our Area Of Interest. The UP42_challenge.geojson file specifies a polygon area on Taormina coast in Sicily, Italy.

Following are the contents of the geojson file:
TODO: Fix this code sample

```json
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "properties": {
        "stroke": "#555555",
        "stroke-width": 2,
        "stroke-opacity": 1,
        "fill": "#555555",
        "fill-opacity": 0.5
      },
      "geometry": {
        "type": "Polygon",
        "coordinates": [
          [
            [
              15.282325744628906,
              37.85405097280397
            ],
            [
              15.281896591186525,
              37.84327477258804
            ],
            [
              15.301208496093748,
              37.843139212870334
            ],
            [
              15.301809310913086,
              37.85357658203691
            ],
            [
              15.282325744628906,
              37.85405097280397
            ]
          ]
        ]
      }
    }
  ]
}
```

|   |   |
|---|---|
 Request  Type | POST | 
 URL | https://api.up42.com/projects/{project_id}/workflows/{workflow_id}/jobs| | 
 Authorization | [Bearer token](https://geospatialapis.stoplight.io/docs/processing-satellite-imagery-using-up42-apis/scgg70a0ykpet-2-generate-a-bearer-token-and-copy-its-value) | 
 Body | Raw, JSON|

 ## Sample Request Body/Payload
```json
{
  "aws-s2-l2a:1": {
    "ids": null,
    "time": "2018-12-01T00:00:00+00:00/2021-12-31T23:59:59+00:00",
    "limit": 1,
    "time_series": null,
    "max_cloud_cover": 10,
    "contains": {
      "type": "Polygon",
      "coordinates": [
        [
          [
            15.282326,
            37.854051
          ],
          [
            15.281897,
            37.843275
          ],
          [
            15.301208,
            37.843139
          ],
          [
            15.301809,
            37.853577
          ],
          [
            15.282326,
            37.854051
          ]
        ]
      ]
    }
  },
  "s2-superresolution:1": {
    "bbox": null,
    "contains": null,
    "intersects": null,
    "clip_to_aoi": true,
    "copy_original_bands": true
  }
}
```
**Pro-tip:** Set the clip_to_aoi parameter to true to save on data.  TODO: Add more detail.

**Next step:** [5. Download the Output/Data Processed by the specified Workflow](Download-the-Output.md) 

[Back To The Overview](https://github.com/TheContentGym/GeospatialAPIs-UP42/blob/main/Overview.md)