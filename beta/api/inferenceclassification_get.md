# Get inferenceClassification

Retrieve the properties and relationships of inferenceclassification object.
### Prerequisites
The following **scopes** are required to execute this API: 
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
GET /users/<objectId>/inferenceClassification
GET /drive/root/createdByUser/inferenceClassification
GET /drive/root/lastModifiedByUser/inferenceClassification
```
### Optional query parameters
This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.

### Request headers
| Name       | Type | Description|
|:-----------|:------|:----------|
| Authorization  | string  | Bearer <token>. Required. |

### Request body
Do not supply a request body for this method.
### Response
If successful, this method returns a `200 OK` response code and [inferenceClassification](../resources/inferenceclassification.md) object in the response body.
### Example
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "get_inferenceclassification"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/inferenceClassification
```
##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.inferenceclassification"
} -->
```http
Content-type: application/json
Content-length: 22

{
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get inferenceClassification",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->