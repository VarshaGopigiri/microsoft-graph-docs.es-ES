---
title: Lista decisiones de accessReview
description: En el anuncio de Azure access revisa la característica, recuperar las decisiones de un objeto accessReview.
ms.openlocfilehash: d8cf89706f053dfee6e98cdf23d2539874ac6997
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084353"
---
# <a name="list-accessreview-decisions"></a>Lista decisiones de accessReview

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

En la característica de [acceso revisa](../resources/accessreviews-root.md) Azure AD, recuperar las decisiones de un objeto [accessReview](../resources/accessreview.md) .

Tenga en cuenta que una revisión periódica de acceso no tendrá un `decisions` relación.  En su lugar, debe navegar el autor de la llamada la `instance` relación para buscar un `accessReview` objeto para una instancia actual o pasada de la revisión de access.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso                        | Permisos (de menos a más privilegiados)              |
|:--------------------------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa)     | `AccessReview.Read.All`, `AccessReview.ReadWrite.All`.  También debe ser el usuario iniciado en un rol de Active directory que le permita leer una revisión de acceso. |
|Delegado (cuenta personal de Microsoft) | No admitida. |
|Aplicación                            | No admitida. |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
GET /accessReviews('{reviewId}')/decisions
```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre         | Tipo        | Descripción |
|:-------------|:------------|:------------|
| Authorization | string | Bearer \{token\}. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud
No se debe suministrar ningún cuerpo de la solicitud.

## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `200, OK` código de respuesta y una matriz de objetos de [accessReviewDecision](../resources/accessreviewdecision.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud

<!-- {
  "blockType": "request",
  "name": "get_accessReview_decisions"
}-->
```http
GET https://graph.microsoft.com/beta/accessReviews('2b83cc42-09db-46f6-8c6e-16fec466a82d')/decisions
```

##### <a name="response"></a>Respuesta
>**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.accessReviewDecision",
  "isCollection": "true"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "value":[
    {
            "id": "2b83cc42-09db-46f6-8c6e-16fec466a82d",
            "accessReviewId": "2b83cc42-09db-46f6-8c6e-16fec466a82d",
            "reviewResult": "Approve",
            "userPrincipalName": "alice@litware.com",
            "userId": "Alice Smith"
    }
    ]
}
```

## <a name="see-also"></a>Vea también

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener accessReview](accessreview-get.md) |  [accessReview](../resources/accessreview.md) |  Recuperar una revisión de access. |
|[Mis decisiones accessReview de lista](accessreview-listmydecisions.md) |        colección de [accessReviewDecision](../resources/accessreviewdecision.md)|    Como revisor, obtener Mis decisiones de un accessReview.|
|[Enviar aviso de accessReview](accessreview-sendreminder.md) |       Ninguna.   |   Enviar un aviso a los revisores de un accessReview. |
|[Detener accessReview](accessreview-stop.md) |        Ninguna.   |   Detener una accessReview. |
|[Restablecer las decisiones de accessReview](accessreview-reset.md) |        Ninguna.   |   Restablecer las decisiones en un accessReview en curso.|
|[Aplicar decisiones accessReview](accessreview-apply.md) |        Ninguna.   |   Se aplican las decisiones de un accessReview completado.|


<!-- {
  "type": "#page.annotation",
  "description": "Get accessReview decisions",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
