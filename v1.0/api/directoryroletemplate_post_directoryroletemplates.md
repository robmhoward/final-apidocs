# Create directoryRoleTemplate

Use this API to create a new directoryRoleTemplate.
### Prerequisites
One of the following **scopes** is required to execute this API: 
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
POST /directoryRoles

```
### Request headers
| Name       | Type | Description|
|:---------------|:--------|:----------|
| Authorization  | string  | Bearer <token>. Required. |

### Request body
In the request body, supply a JSON representation of [directoryRoleTemplate](../resources/directoryroletemplate.md) object.


### Response
If successful, this method returns `201, Created` response code and [directoryRoleTemplate](../resources/directoryroletemplate.md) object in the response body.

### Example
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "create_directoryroletemplate_from_directoryroletemplates"
}-->
```http
POST https://graph.microsoft.com/v1.0/directoryRoleTemplates
Content-type: application/json
Content-length: 115

{
  "directoryRoleTemplate": {
    "description": "description-value",
    "displayName": "displayName-value"
  }
}
```
In the request body, supply a JSON representation of [directoryRoleTemplate](../resources/directoryroletemplate.md) object.
##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryroletemplate"
} -->
```http
Content-type: application/json
Content-length: 137

{
  "directoryRoleTemplate": {
    "description": "description-value",
    "displayName": "displayName-value",
    "id": "id-value"
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create directoryRoleTemplate",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->