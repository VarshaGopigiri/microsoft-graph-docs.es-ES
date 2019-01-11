---
title: Obtener las actividades del usuario
description: Obtener las actividades de un usuario determinado. A diferencia de la **reciente** OData (función), se devolverán las actividades sin historiales. El permiso UserActivity.ReadWrite.CreatedByApp se aplicará filtrado adicional a la respuesta, para que se devuelvan únicamente las actividades creadas por la aplicación. Este filtrado del lado del servidor, se podría producir páginas vacías si el usuario está especialmente activo y otras aplicaciones han creado actividades más recientes. Para obtener las actividades de la aplicación, utilice la propiedad **nextLink** a paginar.
localization_priority: Normal
ms.openlocfilehash: 8106d1c2cb740033fd81a21068aba5a15fd1b1b5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27809376"
---
# <a name="get-user-activities"></a>Obtener las actividades del usuario

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Obtener las actividades de un usuario determinado. A diferencia de la **reciente** OData (función), se devolverán las actividades sin historiales. El permiso UserActivity.ReadWrite.CreatedByApp se aplicará filtrado adicional a la respuesta, para que se devuelvan únicamente las actividades creadas por la aplicación. Este filtrado del lado del servidor, se podría producir páginas vacías si el usuario está especialmente activo y otras aplicaciones han creado actividades más recientes. Para obtener las actividades de la aplicación, utilice la propiedad **nextLink** a paginar.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | UserActivity.ReadWrite.CreatedByApp    |
|Delegado (cuenta personal de Microsoft) | UserActivity.ReadWrite.CreatedByApp    |
|Aplicación | No admitida. |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
GET /me/activities
```

## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales

Este método es compatible con algunos de [Los parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) para ayudar a personalizar la respuesta. Se admiten los siguientes parámetros de consulta:

- Expanda $ para la propiedad de navegación **historyItems** .
- $top para limitar el número máximo de elementos en las páginas.
- $filter en la propiedad **lastModifiedDateTime** para **actividades** o **historyItems**, si expandida.

Los siguientes son algunos ejemplos de consultas compatibles con codificación URL:

```
/me/activities?$expand=historyItems($filter=lastModifiedDateTime%20gt%202018-01-22T21:45:00.347Z%20and%20lastModifiedDateTime%20lt%202018-01-22T22:00:00.347Z)

/me/activities?$filter=lastModifiedDateTime%20lt%202018-01-16T01:03:21.347Z%20and%20lastModifiedDateTime%20gt%202018-01-03T01:03:21.347Z

/me/activities?$top=5
```

## <a name="request-headers"></a>Encabezados de solicitud

|Nombre | Tipo | Descripción|
|:----|:-----|:-----------|
|Autorización | string | {token} de portador. Obligatorio.|

## <a name="request-body"></a>Cuerpo de la solicitud

Ningún cuerpo de la solicitud.

## <a name="response"></a>Respuesta

Si tiene éxito, este método devuelve el `200 OK` código de respuesta con las actividades del usuario para la aplicación.

## <a name="example"></a>Ejemplo

##### <a name="request"></a>Solicitud

Aquí tiene un ejemplo de la solicitud.

<!-- {
  "blockType": "ignored",
  "name": "get_activities"
}-->

```http
GET https://graph.microsoft.com/beta/me/activities
```

##### <a name="response"></a>Respuesta

Este es un ejemplo de la respuesta.

<!-- {
  "blockType": "ignored",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.activity)"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(userActivity)",
    "@odata.nextLink": "https://graph.microsoft.com/beta/me/activities?$skiptoken=%24filter%3dlastModifiedDateTime+lt+2018-02-26T18%3a06%3a19.365Z",
    "value": [{
        "@odata.type": "#microsoft.graph.activity",
        "activitySourceHost": "https://www.contoso.com",
        "createdDateTime": "2018-02-26T18:34:29.592Z",
        "lastModifiedDateTime": "2018-02-26T18:34:29.607Z",
        "id": "5347642601316252694",
        "appActivityId": "/article?12345",
        "visualElements": {
            "attribution": {
              "iconUrl": "https://www.contoso.com/icon",
              "alternateText": "Contoso, Ltd.",
              "addImageQuery": "false",
              },
            "displayText": "Contoso How-To: How to Tie a Reef Knot",
            "description": "How to Tie a Reef Knot. A step-by-step visual guide to the art of nautical knot-tying.",
            "backgroundColor": "#ff0000",
            "content": {
              "$schema": "https://adaptivecards.io/schemas/adaptive-card.json",
              "type": "AdaptiveCard",
              "body":
              [{
                  "type": "TextBlock",
                  "text": "Contoso MainPage"
              }]
            }
        },
        "activationUrl": "https://www.contoso.com/article?id=12345",
        "appDisplayName": "Contoso, Ltd.",
        "userTimezone": "Africa/Casablanca",
        "fallbackUrl": "https://www.contoso.com/article?id=12345",
        "contentUrl": "https://www.contoso.com/article?id=12345",
        "contentInfo": {
            "@context": "https://schema.org",
            "@type": "Article",
            "author": "John Doe",
            "name": "How to Tie a Reef Knot"
        },
        "expirationDateTime": "2018-03-28T18:34:29.607Z",
        "status": "updated"
    }]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2017-06-07 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get activities",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
