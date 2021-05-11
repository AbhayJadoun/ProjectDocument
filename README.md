**API to get filtered CRM Data**
----

Fetching Result CRM data on the basis of the filter request json.

<details>  

* **URL**

  /api/{tenantId}/CRMData/getResultCRMData

* **Method:**

	`POST`
  
*  **URL Params**

	**Required:**
 
   	`tenantId=[GUID]`

   

* **Data Params**

  **CRMResultData:**
  
  `{`
			`id		string`	
					`nullable: true`
			`label	string` 	
					`nullable: true` 
					`readOnly: true`
			`edge	string` 	
					`nullable: true`
			`filters	[`		
					`nullable: true`
				`Filter{`
						`field		string` 
									`nullable: true` 
						`operator	string` 
									`nullable: true` 
						`value		string` 
									`nullable: true`
					`}`
				`]`
				`order	{`
					`< * >:	string`
				`}`		
				`nullable: true`
	`}`
* **Success Response:**
 
  * **Code:** 200 <br />
  * **Content:** 
    
```json
        [
          { 
            "ActivityType": "Meeting", 
            "Subject": "Financial Pertner Meeting", 
            "Date": "1620376676", 
            "Regarding": "Anacap Financial Partner", 
            "Owner": "Ravina", 
            "Location": "Meeting room, churchill" 
          }
        ]
```


* **Sample Call:**
```json
	{
	  "id": "string",
	  "edge": "string",
	  "filters": [
		{
		  "field": "ActivityType",
		  "operator": "eq",
		  "value": "Phone Call"
		}
	  ],
	  "order": {
		"Date": "incr"
	  }
	}
 ``` 

* **Notes:**
</details>
