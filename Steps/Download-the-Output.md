
# 6. Download the Output/Data Processed by the specified Workflow  

After your job is complete, you can download the data processed by the workflow you specified. 

**Protip:** You can use webhooks to set up alert for completion of your workflow processing. 

## URL and Parameters

|   |   |
|---|---|
 Request  Type | GET | 
 URL | https://api.up42.com/projects/{project_id}/jobs/{job_id}/tasks/{task_id}/downloads/results| | 
 Authorization | [Bearer token](https://geospatialapis.stoplight.io/docs/processing-satellite-imagery-using-up42-apis/scgg70a0ykpet-2-generate-a-bearer-token-and-copy-its-value) | 




## Sample Response
```json
{
    "data": {
        "url": "https://storage.googleapis.com/interstellar-prod-processing-artifacts/01db9695-6991-48e7-b45f-be0217354198/01db9695-6991-48e7-b45f-be0217354198-3270721306/output.tgz?GoogleAccessId=prod-application-cluster@interstellar-prod-env.iam.gserviceaccount.com&Expires=1654277798&Signature=iMTEH%2FSgD9uKVQusPlK3PELFljTnNIZBfRci2m0FHoN0HHV125zPR%2Bn16%2FAyxIldRHfU%2B51vQx8KspR88yr5ESZEqf725coEBFJTSOwjI6%2Bbb2v%2BhLXvXVwhdU7KKTWiPNs38x%2FiSXJGXBOj%2Baiufq6GyoqLZq4gfTPVWqmrCiQsaP61EIwudr7LSDhAnxWAUeo%2FZCgzMlnZR%2FJMMqyI%2FKEgNTXgUgV3i0x%2Fjg48Vy%2FoshM%2B02%2F77GBXZhOHBYrsE8rK72k8FC543Z6NV7n4Sf0oZvu2LwX7IHb6qLl7VJVvccCoNqLm0h3pCp32wt0qo9FEgOS1ohO73aGbL9Ytag%3D%3D"
    },
    "error": null
}

```

Use the URL to download the processed data. 

**Final Step:** [6. Visualize the data in QGIS](Download-QGIS-and-Visualize-the-Downloaded-Data.md) 

***
Back To:  

-[Overview](https://github.com/TheContentGym/GeospatialAPIs-UP42/blob/main/Overview.md)  
-[Readme](https://github.com/TheContentGym/GeospatialAPIs-UP42/blob/main/README.md) 
***