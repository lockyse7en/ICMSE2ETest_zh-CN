# <a name="list-notebooks"></a>列表的笔记本

检索的[笔记本](../resources/notebook.md)对象的列表。
## <a name="prerequisites"></a>先决条件
以下**范围**之一是执行此 API 所需的︰  
Notes.Read、 Notes.ReadWrite.CreatedByApp、 Notes.ReadWrite、 Notes.Read.All 或 Notes.ReadWrite.All 
## <a name="http-request"></a>HTTP 请求
<!-- { "blockType": "ignored" } -->
```http
GET /me/notes/notebooks
GET /users/<id | userPrincipalName>/notes/notebooks
GET /groups/<id>/notes/notebooks
```
## <a name="optional-query-parameters"></a>可选的查询参数
此方法支持[OData 查询参数](http://graph.microsoft.io/docs/overview/query_parameters)来帮助自定义响应。

默认的排序顺序为`name asc`。 

有效`expand`的值的笔记本是`sections`， `sectionGroups`。

## <a name="request-headers"></a>请求标头
| 名称       | 类型 | 说明|
|:-----------|:------|:----------|
| 授权  | string  | `Bearer <token>`对基于用户凭据并无授权访问用户的应用程序提供一个有效 OAuth 标记。 |
| 接受 | string | `application/json` |  

## <a name="request-body"></a>请求正文
请不要提供此方法请求正文。
## <a name="response"></a>响应
如果成功，此方法返回`200 OK`响应代码和[笔记本](../resources/notebook.md)在响应正文中的对象的集合。
## <a name="example"></a>示例
##### <a name="request"></a>请求
下面是示例请求。
<!-- {
  "blockType": "request",
  "name": "get_notebooks"
}-->
```http
GET https://graph.microsoft.com/beta/me/notes/notebooks
```
##### <a name="response"></a>响应
这里是响应的示例。 注意︰ 此处所示的响应对象将被截断为简洁起见。 从实际调用将返回的所有属性。
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.notebook",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 369

{
  "value": [
    {
      "isDefault": true,
      "userRole": {
      },
      "isShared": true,
      "sectionsUrl": "sectionsUrl-value",
      "sectionGroupsUrl": "sectionGroupsUrl-value",
      "links": {
        "oneNoteClientUrl": {
          "href": "href-value"
        },
        "oneNoteWebUrl": {
          "href": "href-value"
        }
      }
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List notebooks",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->