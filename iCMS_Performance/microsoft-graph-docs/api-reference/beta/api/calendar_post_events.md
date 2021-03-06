# <a name="create-event"></a>创建事件

此 API 用于默认或指定的日历中创建新的事件。
## <a name="prerequisites"></a>先决条件
需执行此 API 之一以下**范围**︰ *Calendars.ReadWrite*
## <a name="http-request"></a>HTTP 请求
<!-- { "blockType": "ignored" } -->
用户或组的默认[日历](../resources/calendar.md)。
```http
POST /me/calendar/events
POST /users/<id | userPrincipalName>/calendar/events
POST /groups/<id>/calendar/events
```
[日历](../resources/calendar.md)的用户的默认值[calendarGroup](../resources/calendargroup.md)。
```http
POST /me/calendars/<id>/events
POST /users/<id | userPrincipalName>/calendars/<id>/events

POST /me/calendarGroup/calendars/<id>/events
POST /users/<id | userPrincipalName>/calendarGroup/calendars/<id>/events
```
在特定的[calendarGroup](../resources/calendargroup.md)的用户的[日历](../resources/calendar.md)。
```http
POST /me/calendarGroups/<id>/calendars/<id>/events
POST /users/<id | userPrincipalName>/calendarGroups/<id>/calendars/<id>/events
```
## <a name="request-headers"></a>请求标头
| 页眉       | 值 |
|:---------------|:--------|
| 授权  | 持有者<token>。 必需。  |
| 内容类型  | 应用程序/json。 必需。  |

## <a name="request-body"></a>请求正文
在请求正文中，提供[事件](../resources/event.md)对象的 JSON 的表示。


## <a name="response"></a>响应
如果成功，此方法返回`201, Created`响应代码和[事件](../resources/event.md)对象在响应正文中的。

## <a name="example"></a>示例
##### <a name="request"></a>请求
下面是示例请求。
<!-- {
  "blockType": "request",
  "name": "create_event_from_calendar"
}-->
```http
POST https://graph.microsoft.com/beta/me/calendar/events
Content-type: application/json
Content-length: 285

{
  "originalStartTimeZone": "originalStartTimeZone-value",
  "originalEndTimeZone": "originalEndTimeZone-value",
  "responseStatus": {
    "response": "",
    "time": "datetime-value"
  },
  "reminderMinutesBeforeStart": 99,
  "isReminderOn": true
}
```
在请求正文中，提供[事件](../resources/event.md)对象的 JSON 的表示。
##### <a name="response"></a>响应
这里是响应的示例。 注意︰ 为了简单起见，此处所示的响应对象可能被截断。 从实际调用将返回的所有属性。
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.event"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 285

{
  "originalStartTimeZone": "originalStartTimeZone-value",
  "originalEndTimeZone": "originalEndTimeZone-value",
  "responseStatus": {
    "response": "",
    "time": "datetime-value"
  },
  "iCalUId": "iCalUId-value",
  "reminderMinutesBeforeStart": 99,
  "isReminderOn": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Event",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
