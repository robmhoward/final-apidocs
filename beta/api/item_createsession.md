# item: createSession


### Prerequisites
The following **scopes** are required to execute this API: 
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
POST /drive/root/Microsoft.Graph.createSession
POST /drive/items/<id>/Microsoft.Graph.createSession
POST /drives/<id>/root/Microsoft.Graph.createSession

```
### Request headers
| Name       | Type | Description|
|:---------------|:--------|:----------|
| Authorization  | string  | Bearer <token>. Required. |

### Request body
In the request body, provide a JSON object with the following parameters.

| Parameter	   | Type	|Description|
|:---------------|:--------|:----------|
|item|chunkedUploadSessionDescriptor||

### Response
If successful, this method returns `200, OK` response code and [uploadSession](../resources/uploadsession.md) object in the response body.

### Example
Here is an example of how to call this API.
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "item_createsession"
}-->
```http
POST https://graph.microsoft.com/beta/drive/root/Microsoft.Graph.createSession
Content-type: application/json
Content-length: 44

{
  "item": {
    "name": "name-value"
  }
}
```

##### Response
Here is an example of the response.
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.uploadsession"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 140

{
  "uploadUrl": "uploadUrl-value",
  "expirationDateTime": "datetime-value",
  "nextExpectedRanges": [
    "nextExpectedRanges-value"
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "item: createSession",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->