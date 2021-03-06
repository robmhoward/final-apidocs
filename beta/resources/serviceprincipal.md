# servicePrincipal resource type

Represents an instance of an application in a directory. Inherits from [DirectoryObject].


### JSON representation

Here is a JSON representation of the resource

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "appRoleAssignedTo",
    "appRoleAssignments",
    "createdObjects",
    "createdOnBehalfOf",
    "memberOf",
    "oauth2PermissionGrants",
    "ownedObjects",
    "owners"
  ],
  "@odata.type": "microsoft.graph.serviceprincipal"
}-->

```json
{
  "accountEnabled": true,
  "addIns": [{"@odata.type": "microsoft.graph.addIn"}],
  "appDisplayName": "string",
  "appId": "string",
  "appOwnerOrganizationId": "guid",
  "appRoleAssignmentRequired": true,
  "appRoles": [{"@odata.type": "microsoft.graph.appRole"}],
  "displayName": "string",
  "errorUrl": "string",
  "homepage": "string",
  "id": "string (identifier)",
  "keyCredentials": [{"@odata.type": "microsoft.graph.keyCredential"}],
  "logoutUrl": "string",
  "oauth2Permissions": [{"@odata.type": "microsoft.graph.oAuth2Permission"}],
  "passwordCredentials": [{"@odata.type": "microsoft.graph.passwordCredential"}],
  "preferredTokenSigningKeyThumbprint": "string",
  "publisherName": "string",
  "replyUrls": ["string"],
  "samlMetadataUrl": "string",
  "servicePrincipalNames": ["string"],
  "tags": ["string"]
}

```
### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|accountEnabled|Boolean|                **true** if the service principal account is enabled; otherwise, **false**.            |
|appDisplayName|String|The display name exposed by the associated application.|
|appId|String|The unique identifier for the associated application (its **appId** property).|
|appRoleAssignmentRequired|Boolean|Specifies whether an **AppRoleAssignment** to a user or group is required before Azure AD will issue a user or access token to the application.                            **Notes**: Requires version 1.5 or newer, not nullable.            |
|appRoles|[AppRole](approle.md) collection|The application roles exposed by the associated application. For more information see the **appRoles** property definition on the [Application] entity                            **Notes**: Requires version 1.5 or newer, not nullable.            |
|displayName|String|The display name for the service principal.|
|errorUrl|String|            |
|homepage|String|The URL to the homepage of the associated   application.|
|keyCredentials|[KeyCredential](keycredential.md) collection|The collection of key credentials associated with the service principal.                            **Notes**: not nullable.            |
|logoutUrl|String|            |
|oauth2Permissions|[OAuth2Permission](oauth2permission.md) collection|The OAuth 2.0 permissions exposed by the associated application. For more information see the **oauth2Permissions** property definition on the [Application] entity.                            **Notes**: Requires version 1.5 or newer, not nullable.            |
|id|String|The unique identifier for the service principal. Inherited from [DirectoryObject].                            **Notes**: **key**, immutable, not nullable, unique.             Read-only.|
|passwordCredentials|[PasswordCredential](passwordcredential.md) collection|The collection of password credentials associated with the service principal.                            **Notes**: not nullable.            |
|preferredTokenSigningKeyThumbprint|String|Reserved for internal use only. Do not write or otherwise rely on this property. May be removed in future versions.                            **Notes**: Requires version 1.5 or newer.            |
|publisherName|String|The display name of the tenant in which the associated application is specified.|
|replyUrls|String collection|The URLs that user tokens are sent to for sign in with the associated application, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to for the associated application.                            **Notes**: not nullable.            |
|samlMetadataUrl|String|            |
|servicePrincipalNames|String collection|The URIs that identify the associated application. For more information see, [Application Objects and Service Principal Objects](https://msdn.microsoft.com/en-us/library/azure/dn132633.aspx).                            **Notes**: not nullable, the **any** operator is required for filter expressions on multi-valued properties; for more information, see [Supported Queries, Filters, and Paging Options](https://msdn.microsoft.com/library/azure/dn727074.aspx).            |
|tags|String collection|                                        **Notes**: not nullable.            |

### Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|appRoleAssignedTo|[AppRoleAssignment](approleassignment.md)|Principals (users, groups, and service principals) that are assigned to this service principal. Requires version 1.5 or newer. Read-only.|
|appRoleAssignments|[AppRoleAssignment](approleassignment.md) collection|Applications that the service principal is assigned to. Requires version 1.5 or newer. Read-only. Nullable.|
|createdObjects|[DirectoryObject](directoryobject.md) collection|Directory objects created by this service principal. Inherited from [DirectoryObject]. Requires version 2013-11-08 or newer. Read-only. Nullable.|
|memberOf|[DirectoryObject](directoryobject.md) collection|Roles that this service principal is a member of. Inherited from [DirectoryObject].            HTTP Methods: GET Read-only. Nullable.|
|oauth2PermissionGrants|[OAuth2PermissionGrant](oauth2permissiongrant.md) collection|User impersonation grants associated with this service principal. Requires version 1.5 or newer. Read-only. Nullable.|
|ownedObjects|[DirectoryObject](directoryobject.md) collection|Directory objects that are owned by this service principal. Inherited from [DirectoryObject]. Requires version 2013-11-08 or newer. Read-only. Nullable.|
|owners|[DirectoryObject](directoryobject.md) collection|Directory objects that are owners of this service principal. The owners are a set of non-admin users who are allowed to modify this object. Inherited from [DirectoryObject]. Requires version 2013-11-08 or newer. Read-only. Nullable.|

### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get servicePrincipal](../api/serviceprincipal_get.md) | [servicePrincipal](serviceprincipal.md) |Read properties and relationships of servicePrincipal object.|
|[Create AppRoleAssignment](../api/serviceprincipal_post_approleassignments.md) |[AppRoleAssignment](approleassignment.md)| Create a new AppRoleAssignment by posting to the appRoleAssignments collection.|
|[List appRoleAssignments](../api/serviceprincipal_list_approleassignments.md) |[AppRoleAssignment](approleassignment.md) collection| Get a AppRoleAssignment object collection.|
|[Create createdObject](../api/serviceprincipal_post_createdobjects.md) |[DirectoryObject](directoryobject.md)| Create a new createdObject by posting to the createdObjects collection.|
|[List createdObjects](../api/serviceprincipal_list_createdobjects.md) |[DirectoryObject](directoryobject.md) collection| Get a createdObject object collection.|
|[Create memberOf](../api/serviceprincipal_post_memberof.md) |[DirectoryObject](directoryobject.md)| Create a new memberOf by posting to the memberOf collection.|
|[List memberOf](../api/serviceprincipal_list_memberof.md) |[DirectoryObject](directoryobject.md) collection| Get a memberOf object collection.|
|[Create OAuth2PermissionGrant](../api/serviceprincipal_post_oauth2permissiongrants.md) |[OAuth2PermissionGrant](oauth2permissiongrant.md)| Create a new OAuth2PermissionGrant by posting to the oauth2PermissionGrants collection.|
|[List oauth2PermissionGrants](../api/serviceprincipal_list_oauth2permissiongrants.md) |[OAuth2PermissionGrant](oauth2permissiongrant.md) collection| Get a OAuth2PermissionGrant object collection.|
|[Create ownedObject](../api/serviceprincipal_post_ownedobjects.md) |[DirectoryObject](directoryobject.md)| Create a new ownedObject by posting to the ownedObjects collection.|
|[List ownedObjects](../api/serviceprincipal_list_ownedobjects.md) |[DirectoryObject](directoryobject.md) collection| Get a ownedObject object collection.|
|[Create owner](../api/serviceprincipal_post_owners.md) |[DirectoryObject](directoryobject.md)| Create a new owner by posting to the owners collection.|
|[List owners](../api/serviceprincipal_list_owners.md) |[DirectoryObject](directoryobject.md) collection| Get a owner object collection.|
|[Update](../api/serviceprincipal_update.md) | [servicePrincipal](serviceprincipal.md)	|Update servicePrincipal object. |
|[Delete](../api/serviceprincipal_delete.md) | None |Delete servicePrincipal object. |
|[checkMemberGroups](../api/serviceprincipal_checkmembergroups.md)|String collection||
|[getMemberGroups](../api/serviceprincipal_getmembergroups.md)|String collection||
|[getMemberObjects](../api/serviceprincipal_getmemberobjects.md)|String collection||

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "servicePrincipal resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->