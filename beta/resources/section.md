# section resource type

A section in a OneNote notebook. Sections can contain pages.

### JSON representation

Here is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "pages",
    "parentNotebook",
    "parentSectionGroup"
  ],
  "@odata.type": "microsoft.graph.section"
}-->

```json
{
  "createdBy": "string",
  "createdByIdentity": {"@odata.type": "microsoft.graph.oneNoteIdentitySet"},
  "createdTime": {"@odata.type": "microsoft.graph.dateTimeOffset"},
  "id": "string (identifier)",
  "isDefault": true,
  "lastModifiedBy": "string",
  "lastModifiedByIdentity": {"@odata.type": "microsoft.graph.oneNoteIdentitySet"},
  "lastModifiedTime": {"@odata.type": "microsoft.graph.dateTimeOffset"},
  "name": "string",
  "pagesUrl": "string",
  "self": "string"
}

```
### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|createdBy|String|The user who created the section. Read-only.|
|createdTime|DateTimeOffset|The date and time when the section was created. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.|
|id|String|The unique identifier of the section.  Read-only.|
|isDefault|Boolean|Indicates whether this is the user's default section. Read-only.|
|lastModifiedBy|String|The user who last modified the section. Read-only.|
|lastModifiedTime|DateTimeOffset|The date and time when the section was last modified. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.|
|name|String|The name of the section. |
|pagesUrl|String|The `pages` endpoint where you can get details for all the pages in the section. Read-only.|
|self|String|The endpoint where you can get details about the section. Read-only.|

### Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|pages|[Page](page.md) collection|The collection of pages in the section.  Read-only. Nullable.|
|parentNotebook|[Notebook](notebook.md)|The notebook that contains the section.  Read-only.|
|parentSectionGroup|[SectionGroup](sectiongroup.md)|The section group that contains the section.  Read-only.|

### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get section](../api/section_get.md) | [Section](section.md) |Read the properties and relationships of the section.|
|[Create page](../api/section_post_pages.md) |[Page](page.md)| Create a page by posting to the pages collection in the specified section.|
|[List pages](../api/section_list_pages.md) |[Page](page.md) collection| Get a collection of pages in the specified section.|
|[copyToNotebook](../api/section_copytonotebook.md)|None|Copy the section to a specific notebook.|
|[copyToSectionGroup](../api/section_copytosectiongroup.md)|None|Copy the section to a specific section group.|


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "section resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->