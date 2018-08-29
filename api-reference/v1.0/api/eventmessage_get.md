# <a name="get-eventmessage"></a>Get eventMessage

Recupera las propiedades y las relaciones del objeto [eventMessage](../resources/eventmessage.md). Aplique el parámetro $expand en la propiedad de navegación de **evento** para obtener el [evento](../resources/event.md) asociado en el calendario del asistente.

Actualmente, esta operación devuelve los cuerpos de los mensajes de evento solo en formato HTML.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Mail.Read    |
|Delegado (cuenta personal de Microsoft) | Mail.Read    |
|Aplicación | Mail.Read |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
GET /me/messages/{id}
GET /users/{id | userPrincipalName}/messages/{id}

GET /me/mailFolders/{id}/messages/{id}
GET /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}
```
## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales
Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción|
|:-----------|:------|:----------|
| Authorization  | cadena  | {token} de portador. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [eventMessage](../resources/eventmessage.md) en el cuerpo de la respuesta.
## <a name="example"></a>Ejemplo
##### <a name="request-1"></a>Solicitud 1
En el primer ejemplo, se muestra cómo obtener las propiedades de un mensaje de evento a partir del id. del mensaje de evento.
<!-- {
  "blockType": "request",
  "sampleKeys": ["AAMkADYAAAImV_lAAA="],
  "name": "get_eventmessage"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/messages/AAMkADYAAAImV_lAAA=
```
##### <a name="response-1"></a>Respuesta 1
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "name": "get_eventmessage",
  "truncated": true,
  "@odata.type": "microsoft.graph.eventMessage"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users('8fd6e83b-3cc0-4bf0-8b26-950f4d7110f6')/messages/$entity",
    "@odata.type":"#microsoft.graph.eventMessage",
    "@odata.etag":"W/\"CwAAABYAAABXlB/SL0N4Q6g6o+jSYAEuAAAImkVD\"",
    "id":"AAMkADYAAAImV_lAAA=",
    "createdDateTime":"2017-12-27T21:58:36Z",
    "lastModifiedDateTime":"2017-12-27T23:26:38Z",
    "changeKey":"CwAAABYAAABXlB/SL0N4Q6g6o+jSYAEuAAAImkVD",
    "categories":[

    ],
    "receivedDateTime":"2017-12-27T21:58:36Z",
    "sentDateTime":"2017-12-27T21:58:36Z",
    "hasAttachments":false,
    "internetMessageId":"<MWHPR1301MB2110DCFC@MWHPR1301MB2110.namprd13.prod.outlook.com>",
    "subject":"Debrief from meetup",
    "bodyPreview":"Let's debrief after community meetup.",
    "importance":"normal",
    "parentFolderId":"AQMkADYAAAIBDAAAAA==",
    "conversationId":"AAQkADYCipTiRjXQORU=",
    "isDeliveryReceiptRequested":null,
    "isReadReceiptRequested":false,
    "isRead":false,
    "isDraft":false,
    "webLink":"https://outlook.office365.com/owa/?ItemID=AAMkADYAAAImV%2BlAAA%3D&exvsurl=1&viewmodel=ReadMessageItem",
    "inferenceClassification":"focused",
    "meetingMessageType":"meetingRequest",
    "body":{
        "contentType":"html",
        "content":"<html>\r\n<head>\r\n<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n<meta content=\"text/html; charset=us-ascii\">\r\n<style type=\"text/css\" style=\"display:none\">\r\n<!--\r\np\r\n\t{margin-top:0;\r\n\tmargin-bottom:0}\r\n-->\r\n</style>\r\n</head>\r\n<body dir=\"ltr\">\r\n<div id=\"divtagdefaultwrapper\" dir=\"ltr\" style=\"font-size:12pt; color:#000000; font-family:Calibri,Helvetica,sans-serif\">\r\n<p style=\"margin-top:0; margin-bottom:0\">Let's debrief after community meetup.<br>\r\n</p>\r\n</div>\r\n</body>\r\n</html>\r\n"
    },
    "sender":{
        "emailAddress":{
            "name":"Administrator",
            "address":"admin@contoso.onmicrosoft.com"
        }
    },
    "from":{
        "emailAddress":{
            "name":"Administrator",
            "address":"admin@contoso.onmicrosoft.com"
        }
    },
    "toRecipients":[
        {
            "emailAddress":{
                "name":"Alex Wilber",
                "address":"AlexW@contoso.onmicrosoft.com"
            }
        }
    ],
    "ccRecipients":[

    ],
    "bccRecipients":[

    ],
    "replyTo":[

    ]
}
```

##### <a name="request-2"></a>Solicitud 2
En el segundo ejemplo, se muestra cómo obtener el evento asociado a un mensaje. Usa el id. del mensaje de evento para obtener el mensaje de evento, proporciona explícitamente una conversión en el mensaje de evento para obtener acceso a su propiedad de navegación de **evento** y aplica un parámetro $expand para obtener las propiedades del evento.
<!-- {
  "blockType": "request",
  "sampleKeys": ["AAMkADYAAAImV_jAAA="],
  "name": "get_event_based_on_eventmessage"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/messages/AAMkADYAAAImV_jAAA=?$expand=microsoft.graph.eventMessage/event
```
##### <a name="response-2"></a>Respuesta 2
Este es un ejemplo de la respuesta. Las propiedades del evento asociado se devuelven en la respuesta. Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán desde una llamada real.
<!-- {
  "blockType": "response",
  "name": "get_event_based_on_eventmessage",
  "truncated": true,
  "@odata.type": "microsoft.graph.eventMessage"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
   "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users('8fd6e83b-3cc0-4bf0-8b26-950f4d7110f6')/messages/$entity",
   "@odata.type":"#microsoft.graph.eventMessage",
   "@odata.etag":"W/\"CwAAABYAAABXlB/SL0N4Q6g6o+jSYAEuAAAImkVF\"",
   "id":"AAMkADYAAAImV_jAAA=",
   "createdDateTime":"2017-12-27T21:54:55Z",
   "lastModifiedDateTime":"2017-12-27T23:26:38Z",
   "changeKey":"CwAAABYAAABXlB/SL0N4Q6g6o+jSYAEuAAAImkVF",
   "categories":[

   ],
   "receivedDateTime":"2017-12-27T21:54:55Z",
   "sentDateTime":"2017-12-27T21:54:54Z",
   "hasAttachments":false,
   "internetMessageId":"<MWHPR1301MB211042CF@MWHPR1301MB2110.namprd13.prod.outlook.com>",
   "subject":"Kick off planning",
   "bodyPreview":"Let's collect opinions from our teams and organize action items.",
   "importance":"normal",
    "parentFolderId":"AQMkADYAS4AAAIBDAAAAA==",
    "conversationId":"AAQkADYRuffB3wDlPn-ReFZarI60=",
   "isDeliveryReceiptRequested":null,
   "isReadReceiptRequested":false,
   "isRead":false,
   "isDraft":false,
   "webLink":"https://outlook.office365.com/owa/?ItemID=AAMkADYAAAImV%2BjAAA%3D&exvsurl=1&viewmodel=ReadMessageItem",
   "inferenceClassification":"focused",
   "meetingMessageType":"meetingRequest",
   "body":{
      "contentType":"html",
      "content":"<html>\r\n<head>\r\n<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n<meta content=\"text/html; charset=us-ascii\">\r\n<style type=\"text/css\" style=\"display:none\">\r\n<!--\r\np\r\n\t{margin-top:0;\r\n\tmargin-bottom:0}\r\n-->\r\n</style>\r\n</head>\r\n<body dir=\"ltr\">\r\n<div id=\"divtagdefaultwrapper\" dir=\"ltr\" style=\"font-size:12pt; color:#000000; font-family:Calibri,Helvetica,sans-serif\">\r\n<p style=\"margin-top:0; margin-bottom:0\">Let's collect opinions from our teams and organize action items.<br>\r\n</p>\r\n</div>\r\n</body>\r\n</html>\r\n"
   },
   "sender":{
      "emailAddress":{
         "name":"Administrator",
         "address":"admin@contoso.onmicrosoft.com"
      }
   },
   "from":{
      "emailAddress":{
         "name":"Administrator",
         "address":"admin@contoso.onmicrosoft.com"
      }
   },
   "toRecipients":[
      {
         "emailAddress":{
            "name":"Alex Wilber",
            "address":"AlexW@contoso.onmicrosoft.com"
         }
      }
   ],
   "ccRecipients":[

   ],
   "bccRecipients":[

   ],
   "replyTo":[

   ],
   "event@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users('8fd6e83b-3cc0-4bf0-8b26-950f4d7110f6')/messages('AAMkADYAAAImV_jAAA%3D')/microsoft.graph.eventMessage/event/$entity",
   "event":{
      "@odata.etag":"W/\"V5Qf0i9DeEOoOqPo0mABLgAACJpBWg==\"",
      "id":"AAMkADYAAAImVu6AAA=",
      "createdDateTime":"2017-12-27T21:54:55.2624551Z",
      "lastModifiedDateTime":"2017-12-27T22:19:16.6667889Z",
      "changeKey":"V5Qf0i9DeEOoOqPo0mABLgAACJpBWg==",
      "categories":[

      ],
      "originalStartTimeZone":"Pacific Standard Time",
      "originalEndTimeZone":"Pacific Standard Time",
      "iCalUId":"040000008200E00074C5B7101A82E00800000000A2A6F3535D7FD3010000000000000000100000003D770E2E8974F44B9471BDB348097FE3",
      "reminderMinutesBeforeStart":15,
      "isReminderOn":true,
      "hasAttachments":false,
      "subject":"Kick off planning",
      "bodyPreview":"Let's collect opinions from our teams and organize action items.",
      "importance":"normal",
      "sensitivity":"normal",
      "isAllDay":false,
      "isCancelled":false,
      "isOrganizer":false,
      "responseRequested":true,
      "seriesMasterId":null,
      "showAs":"tentative",
      "type":"singleInstance",
      "webLink":"https://outlook.office365.com/owa/?itemid=AAMkADYAAAImVu6AAA%3D&exvsurl=1&path=/calendar/item",
      "onlineMeetingUrl":null,
      "responseStatus":{
         "response":"tentativelyAccepted",
         "time":"2017-12-27T22:19:12.6197462Z"
      },
      "body":{
         "contentType":"html",
         "content":"<html>\r\n<head>\r\n<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n<meta content=\"text/html; charset=us-ascii\">\r\n<style type=\"text/css\" style=\"display:none\">\r\n<!--\r\np\r\n\t{margin-top:0;\r\n\tmargin-bottom:0}\r\n-->\r\n</style>\r\n</head>\r\n<body dir=\"ltr\">\r\n<div id=\"divtagdefaultwrapper\" dir=\"ltr\" style=\"font-size:12pt; color:#000000; font-family:Calibri,Helvetica,sans-serif\">\r\n<p style=\"margin-top:0; margin-bottom:0\">Let's collect opinions from our teams and organize action items.<br>\r\n</p>\r\n</div>\r\n</body>\r\n</html>\r\n"
      },
      "start":{
         "dateTime":"2018-02-02T22:00:00.0000000",
         "timeZone":"UTC"
      },
      "end":{
         "dateTime":"2018-02-02T23:00:00.0000000",
         "timeZone":"UTC"
      },
      "location":{
         "displayName":"Mt. Hood"
      },
      "recurrence":null,
      "attendees":[
         {
            "type":"required",
            "status":{
               "response":"none",
               "time":"0001-01-01T00:00:00Z"
            },
            "emailAddress":{
               "name":"Administrator",
               "address":"admin@contoso.onmicrosoft.com"
            }
         },
         {
            "type":"required",
            "status":{
               "response":"tentativelyAccepted",
               "time":"0001-01-01T00:00:00Z"
            },
            "emailAddress":{
               "name":"Alex Wilber",
               "address":"AlexW@contoso.onmicrosoft.com"
            }
         }
      ],
      "organizer":{
         "emailAddress":{
            "name":"Administrator",
            "address":"admin@contoso.onmicrosoft.com"
         }
      }
   }
}
``` 

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get eventMessage",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
