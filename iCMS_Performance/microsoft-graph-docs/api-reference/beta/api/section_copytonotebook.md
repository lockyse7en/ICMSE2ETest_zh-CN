# <a name="section-copytonotebook"></a>部分︰ copyToNotebook
将分区复制到特定的笔记本。

对于复制操作，请按照异步调用模式︰ 先调用复制操作，并且然后轮询结果的操作终结点。
## <a name="prerequisites"></a>先决条件
以下**范围**之一是执行此 API 所需的︰   
Notes.ReadWrite.CreatedByApp、 Notes.ReadWrite 或 Notes.ReadWrite.All 
## <a name="http-request"></a>HTTP 请求
<!-- { "blockType": "ignored" } -->
```http
POST /me/notes/sections/<id>/copyToNotebook
POST /users/<id | userPrincipalName>/notes/sections/<id>/copyToNotebook
POST /groups/<id>/notes/sections/<id>/copyToNotebook
```
## <a name="request-headers"></a>请求标头
| 名称       | 类型 | 说明|
|:---------------|:--------|:----------|
| 授权  | string  | `Bearer <token>`对基于用户凭据并无授权访问用户的应用程序提供一个有效 OAuth 标记。 |
| 内容类型 | string | `application/json` |

## <a name="request-body"></a>请求正文
在请求正文中，提供了一个 JSON 对象，包含您的操作所需的参数。

| 参数    | 类型   |说明|
|:---------------|:--------|:----------|
|groupId|String|要复制到的组的 id。 只有在复制到 Office 365 组时使用。|
|id|String|必需。 目标笔记本的 id。 |
|renameAs|String|副本的名称。 默认值为现有项的名称。 |

## <a name="response"></a>响应
如果成功，此方法返回`202 Accepted`响应代码和`Operation-Location`头。 轮询操作位置端点获取[复制操作的状态](notesoperation_get.md)。

## <a name="example"></a>示例
这里是如何调用此 API 的示例。
##### <a name="request"></a>请求
下面是示例请求。
<!-- {
  "blockType": "request",
  "name": "section_copytonotebook"
}-->
```http
POST https://graph.microsoft.com/beta/me/notes/sections/<id>/copyToNotebook
Content-type: application/json
Content-length: 84

{
  "id": "id-value",
  "groupId": "groupId-value",
  "renameAs": "renameAs-value"
}
```

##### <a name="response"></a>响应
这里是响应的示例。
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.copystatusmodel"
} -->
```http
HTTP/1.1 202 Accepted
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "section: copyToNotebook",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->