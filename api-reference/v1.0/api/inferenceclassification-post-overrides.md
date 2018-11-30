---
title: Crear inferenceClassificationOverride
description: 'Crear un reemplazo para un remitente identificado por una dirección SMTP. Los mensajes futuros de esa dirección SMTP se clasifica de forma coherente '
ms.openlocfilehash: f068984598ce841b2e7af52c1ed1d25c0e101d10
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031949"
---
# <a name="create-inferenceclassificationoverride"></a>Crear inferenceClassificationOverride

Cree una invalidación para un remitente que se ha identificado mediante una dirección SMTP. Los mensajes futuros de esa dirección SMTP se clasificarán sistemáticamente como se especifica en la invalidación.

**Nota**

- Si ya existe una invalidación con la misma dirección SMTP, los campos **classifyAs** y **name** de esa invalidación se actualizan con los valores proporcionados.
- El número máximo de invalidaciones que admite un buzón es de 1000, basado en direcciones SMTP de remitentes únicos.
- La operación POST solo admite la creación de invalidaciones de una en una.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Mail.ReadWrite    |
|Delegado (cuenta personal de Microsoft) | Mail.ReadWrite    |
|Aplicación | Mail.ReadWrite |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /me/inferenceClassification/overrides
POST /users/{id}/inferenceClassification/overrides
```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción|
|:---------------|:--------|:----------|
| Authorization  | string  | {token} de portador. Obligatorio. |
| Content-Type | string  | Naturaleza de los datos en el cuerpo de una entidad. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione una representación JSON del objeto [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md).

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y un objeto [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "create_inferenceclassificationoverride_from_inferenceclassification"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/inferenceClassification/overrides
Content-type: application/json

{
  "classifyAs": "focused",
  "senderEmailAddress": {
    "name": "Samantha Booth",
    "address": "samanthab@adatum.onmicrosoft.com"
  }
}
```

##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.inferenceClassificationOverride"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
  "classifyAs": "focused",
  "senderEmailAddress": {
    "name": "Samantha Booth",
    "address": "samanthab@adatum.onmicrosoft.com"
  },
  "id": "98f5bdef-576a-404d-a2ea-07a3cf11a9b9"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create inferenceClassificationOverride",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->