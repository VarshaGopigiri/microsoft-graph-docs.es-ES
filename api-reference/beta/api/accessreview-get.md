---
title: Obtener accessReview
description: 'En el anuncio de Azure access revisa la característica, recuperar un objeto accessReview.  '
localization_priority: Normal
ms.openlocfilehash: 471cebe3dbfa60e6cc05e2be546504216163ee0f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27894043"
---
# <a name="get-accessreview"></a>Obtener accessReview

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

En la característica de [acceso revisa](../resources/accessreviews-root.md) Azure AD, recuperar un objeto [accessReview](../resources/accessreview.md) .  

Para recuperar los revisores de la revisión de access, utilice la [lista de revisores accessReview](accessreview-listreviewers.md) API. Para recuperar las decisiones de la revisión de access, utilice la API de [decisiones de accessReview de lista](accessreview-listdecisions.md) o la API de [Mis decisiones accessReview de lista](accessreview-listmydecisions.md) .

Si se trata de una revisión periódica de acceso, a continuación, use la `instances` relación para recuperar una colección de [accessReview](../resources/accessreview.md) de los últimos, instancias actuales y futuros de la revisión de access.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso                        | Permisos (de menos a más privilegiados)              |
|:--------------------------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa)     | `AccessReview.Read.All`, `AccessReview.ReadWrite.All`.  También debe ser el usuario iniciado en un rol de Active directory que le permita leer una revisión de acceso o asignado como un revisor de la revisión de access. |
|Delegado (cuenta personal de Microsoft) | No admitida. |
|Aplicación                            | No admitida. |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
GET /accessReviews('{reviewId}')
```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre         | Tipo        | Descripción |
|:-------------|:------------|:------------|
| Autorización | string | Bearer \{token\}. Necesario. |

## <a name="request-body"></a>Cuerpo de la solicitud
No se debe suministrar ningún cuerpo de la solicitud.

## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `200, OK` código de respuesta y un objeto [accessReview](../resources/accessreview.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud

<!-- {
  "blockType": "request",
  "name": "get_accessReview"
}-->
```http
GET https://graph.microsoft.com/beta/accessReviews('2b83cc42-09db-46f6-8c6e-16fec466a82d')
```

##### <a name="response"></a>Respuesta
>**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.accessReview",
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "id": "2b83cc42-09db-46f6-8c6e-16fec466a82d",
    "displayName": "review",
    "startDateTime": "2017-11-14T01:14:54.89Z",
    "endDateTime": "2017-12-14T01:14:54.89Z",
    "status": "InProgress",
    "businessFlowTemplateId": "6e4f3d20-c5c3-407f-9695-8460952bcc68",
    "reviewerType": "self",
    "description": "",
    "settings": {
        "reviewId": "2b83cc42-09db-46f6-8c6e-16fec466a82d",
        "mailNotificationsEnabled": true,
        "remindersEnabled": true,
        "justificationRequiredOnApproval": true,
        "recurrenceSettings": {
            "recurrenceType": "onetime",
            "recurrenceEndType": "endBy",
            "durationInDays": 0,
            "recurrenceCount": 0
        }
    }
}
```

## <a name="see-also"></a>Vea también

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Crear accessReview](accessreview-create.md) |    [accessReview](../resources/accessreview.md) |  Crear un nuevo accessReview. |
|[Lista programControls](programcontrol-list.md) | colección de [programControl](../resources/programcontrol.md) | ProgramControls de lista en un inquilino. |
|[Revisores accessReview de lista](accessreview-listreviewers.md) |     colección de [IdentidadDeUsuario](../resources/useridentity.md)|    Obtenga los revisores de un accessReview. |
|[Lista decisiones de accessReview](accessreview-listdecisions.md) |     colección de [accessReviewDecision](../resources/accessreviewdecision.md)|    Obtenga las decisiones de un accessReview.|
|[Mis decisiones accessReview de lista](accessreview-listmydecisions.md) |        colección de [accessReviewDecision](../resources/accessreviewdecision.md)|    Como revisor, obtener Mis decisiones de un accessReview.|


<!-- {
  "type": "#page.annotation",
  "description": "Get accessReview",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
