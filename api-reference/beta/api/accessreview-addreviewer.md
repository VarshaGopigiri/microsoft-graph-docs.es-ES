---
title: Agregar revisor accessReview
description: 'En la característica de revisiones de access Azure AD, actualice un objeto accessReview existente para agregar otro usuario como un revisor.  Esta operación sólo se permite para una revisión de acceso que no se ha completado y solo para una revisión de acceso donde se especifican explícitamente los revisores. Esta operación no es permitida para una revisión de access en la que los usuarios revisión su propio acceso y no está pensada para una revisión de access en la que se asignan los propietarios del grupo como los revisores. '
ms.openlocfilehash: ac7722d1bea30659db6f6defe26c0a08ecd67caf
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085647"
---
# <a name="add-accessreview-reviewer"></a>Agregar revisor accessReview

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

En la característica de [acceso revisa](../resources/accessreviews-root.md) Azure AD, actualice un objeto [accessReview](../resources/accessreview.md) existente para agregar otro usuario como un revisor.  Esta operación sólo se permite para una revisión de acceso que no se ha completado y solo para una revisión de acceso donde se especifican explícitamente los revisores. Esta operación no es permitida para una revisión de access en la que los usuarios revisión su propio acceso y no está pensada para una revisión de access en la que se asignan los propietarios del grupo como los revisores. 


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
POST /accessReviews('{reviewId}')/reviewers
```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre         | Tipo        | Descripción |
|:-------------|:------------|:------------|
| Authorization | string | Bearer \{token\}. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcionar una representación JSON del identificador de un usuario que será un revisor.

La siguiente tabla muestran las propiedades que se pueden proporcionar cuando se actualiza un accessReview.

| Propiedad     | Tipo        | Descripción |
|:-------------|:------------|:------------|
| `id`             |`String`                                                        | El identificador de usuario.  |


## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `201, Created` código de respuesta.

## <a name="example"></a>Ejemplo

Éste es un ejemplo de actualización de una única revisión de access (no recurrentes) con un revisor adicional.

##### <a name="request"></a>Solicitud
En el cuerpo de la solicitud, proporcionar una representación JSON del identificador del objeto de usuario.

<!-- {
  "blockType": "request",
  "name": "add_accessReview_reviewer"
}-->
```http
POST https://graph.microsoft.com/beta/accessReviews('2b83cc42-09db-46f6-8c6e-16fec466a82d')/reviewers
Content-type: application/json

{
    "id":"006111db-0810-4494-a6df-904d368bd81b"
}
```

##### <a name="response"></a>Respuesta
>**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 201 Created

```

<!-- {
  "type": "#page.annotation",
  "description": "Add accessReview reviewer",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
