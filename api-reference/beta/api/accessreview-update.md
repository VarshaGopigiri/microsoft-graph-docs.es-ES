---
title: Actualizar accessReview
description: En la característica de revisiones de access Azure AD, actualice un objeto accessReview existente para cambiar una o varias de sus propiedades.
localization_priority: Normal
ms.openlocfilehash: 65420b3682eb9d9f72d95beea624eb84429628ae
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27833750"
---
# <a name="update-accessreview"></a>Actualizar accessReview

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

En la característica de [acceso revisa](../resources/accessreviews-root.md) Azure AD, actualice un objeto [accessReview](../resources/accessreview.md) existente para cambiar una o varias de sus propiedades.

Esta API no está pensada para cambiar los revisores o las decisiones de una revisión.  Para cambiar los revisores, use el [addReviewer](accessreview-addreviewer.md) o [removeReviewer](accessreview-removereviewer.md) API.  Para detener una revisión única ya iniciado, o una instancia ya inició de una revisión periódica, pronto, utilice la [detención](accessreview-stop.md) API y para aplicar las decisiones a los derechos de acceso destino grupo o aplicación, use la [Aplicar](accessreview-apply.md) API. 


## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso                        | Permisos (de menos a más privilegiados)              |
|:--------------------------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa)     | AccessReview.ReadWrite.All |
|Delegado (cuenta personal de Microsoft) | No admitida. |
|Aplicación                            | No admitida. |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
PATCH /accessReviews('{reviewId}')
```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre         | Tipo        | Descripción |
|:-------------|:------------|:------------|
| Autorización | string | Bearer \{token\}. Necesario. |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcionar una representación JSON de parámetros de un objeto [accessReview](../resources/accessreview.md) .

La siguiente tabla muestran las propiedades que se pueden proporcionar cuando se actualiza un accessReview.

| Propiedad     | Tipo        | Description |
|:-------------|:------------|:------------|
| `displayName`             |`String`                                                        | Nombre de la revisión de acceso.  |
| `startDateTime`           |`DateTimeOffset`                                                | La fecha y hora cuando la revisión está programada para que se inicie.  Esto debe ser una fecha en el futuro.   |
| `endDateTime`             |`DateTimeOffset`                                                | La fecha y hora cuando la revisión está programada para finalizar. Esto debe ser al menos un día posterior a la fecha de inicio.   |
| `description`             |`String`                                                        | La descripción, para mostrar a los revisores. |



## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `204, Accepted` código de respuesta y un objeto [accessReview](../resources/accessreview.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

Éste es un ejemplo de actualización de una única revisión de access (no recurrentes).

##### <a name="request"></a>Solicitud
En el cuerpo de la solicitud, proporcionar una representación JSON de las nuevas propiedades del objeto [accessReview](../resources/accessreview.md) .

<!-- {
  "blockType": "request",
  "name": "update_accessReview"
}-->
```http
PATCH https://graph.microsoft.com/beta/accessReviews('006111db-0810-4494-a6df-904d368bd81b')
Content-type: application/json

{
    "displayName":"TestReview new name"
}
```

##### <a name="response"></a>Respuesta
>**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.accessReview"
} -->
```http
HTTP/1.1 204 Accepted
Content-type: application/json

{
    "id": "006111db-0810-4494-a6df-904d368bd81b",
    "displayName": "TestReview new name",
    "startDateTime": "2017-02-10T00:35:53.214Z",
    "endDateTime": "2017-03-12T00:35:53.214Z",
    "status": "Initializing",
    "businessFlowTemplateId": "6e4f3d20-c5c3-407f-9695-8460952bcc68",
    "reviewerType": "delegate",
    "description": "Sample description"
}
```

<!-- {
  "type": "#page.annotation",
  "description": "Update accessReview",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
