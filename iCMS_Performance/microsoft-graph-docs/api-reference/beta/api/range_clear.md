# <a name="range-clear"></a>范围︰ 清除

明确范围值、 格式、 填充、 边框等。
## <a name="prerequisites"></a>先决条件
要执行此 API 需要以下**范围**︰ 
## <a name="http-request"></a>HTTP 请求
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names(<name>)/range/clear
POST /workbook/worksheets(<id|name>)/range(<address>)/clear
POST /workbook/tables(<id|name>)/columns(<id|name>)/range/clear

```
## <a name="request-headers"></a>请求标头
| 名称       | 说明|
|:---------------|:----------|
| 授权  | 持有者<code>|


## <a name="request-body"></a>请求正文
在请求正文中，使用以下参数中提供的 JSON 对象。

| 参数    | 类型   |说明|
|:---------------|:--------|:----------|
|applyTo|string|可选项。 确定清除操作的类型。  可能的值为︰ `All`， `Formats`， `Contents`。|

## <a name="response"></a>响应
如果成功，此方法返回`200, OK`响应代码。 它不返回任何响应正文中。

## <a name="example"></a>示例
这里是如何调用此 API 的示例。
##### <a name="request"></a>请求
下面是示例请求。
<!-- {
  "blockType": "request",
  "name": "range_clear"
}-->
```http
POST https://graph.microsoft.com/beta/me/drive/items/<id>/workbook/names(<name>)/range/clear
Content-type: application/json
Content-length: 32

{
  "applyTo": "applyTo-value"
}
```

##### <a name="response"></a>响应
这里是响应的示例。 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.none"
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Range: clear",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->