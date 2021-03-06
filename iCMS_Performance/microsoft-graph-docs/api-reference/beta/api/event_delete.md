# <a name="delete-event"></a>删除事件

删除事件。
## <a name="prerequisites"></a>先决条件
需执行此 API 之一以下**范围**︰ ***Calendars.ReadWrite***
## <a name="http-request"></a>HTTP 请求
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/events/<id>
DELETE /users/<id | userPrincipalName>/events/<id>
DELETE /groups/<id>/events/<id>

DELETE /me/calendar/events/<id>
DELETE /users/<id | userPrincipalName>/calendar/events/<id>
DELETE /groups/<id>/calendar/events/<id>/

DELETE /me/calendars/<id>/events/<id>
DELETE /users/<id | userPrincipalName>/calendars/<id>/events/<id>

DELETE /me/calendargroup/calendars/<id>/events/<id>
DELETE /users/<id | userPrincipalName>/calendargroup/calendars/<id>/events/<id>

DELETE /me/calendargroups/<id>/calendars/<id>/events/<id>
DELETE /users/<id | userPrincipalName>/calendargroups/<id>/calendars/<id>/events/<id>
```
## <a name="request-headers"></a>请求标头
| 名称       | 类型 | 说明|
|:---------------|:--------|:----------|
| 授权  | string  | 持有者<token>。 必需。 |

## <a name="request-body"></a>请求正文
请不要提供此方法请求正文。


## <a name="response"></a>响应
如果成功，此方法返回`202, Accepted`响应代码。 它不返回任何响应正文中。

## <a name="example"></a>示例
##### <a name="request"></a>请求
下面是示例请求。
<!-- {
  "blockType": "request",
  "name": "delete_event"
}-->
```http
DELETE https://graph.microsoft.com/beta/me/events/<id>
```
##### <a name="response"></a>响应
这里是响应的示例。 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete event",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->