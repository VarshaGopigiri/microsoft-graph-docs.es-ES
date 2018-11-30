---
title: Actualizar inferenceclassificationoverride
description: 'Cambie el campo **classifyAs** de una invalidación tal y como se especifica. '
ms.openlocfilehash: c88b750275a1a3c52edf356ecd93a5c3ba6a3770
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030029"
---
# <a name="update-inferenceclassificationoverride"></a>Actualizar inferenceclassificationoverride

Cambie el campo **classifyAs** de una invalidación tal y como se especifica. 

No puede usar PATCH para cambiar ningún otro campo de una instancia [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md). 

Si hay una invalidación para un remitente y este cambia su nombre para mostrar, puede usar [POST](inferenceclassification-post-overrides.md) para forzar una actualización en el campo de nombre de la invalidación existente.

Si hay una invalidación para un remitente y este cambia su dirección SMTP, la única forma de "actualizar" la invalidación de este remitente es [eliminar](inferenceclassificationoverride-delete.md) la invalidación existente y [crear](inferenceclassification-post-overrides.md) una nueva con la nueva dirección SMTP.

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
PATCH /me/inferenceClassification/overrides/{id}
PATCH /users/{id}/inferenceClassification/overrides/{id}
```

## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción|
|:---------------|:--------|:----------|
| Authorization  | string  | {token} de portador. Obligatorio. |
| Content-Type | string  | Naturaleza de los datos en el cuerpo de una entidad. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione el nuevo valor de **classifyAs**. Para obtener el mejor rendimiento, no debe incluir valores existentes que no cambien.

| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|classifyAs|string| Especifica cómo los mensajes entrantes de una determinada siempre debe clasificarse como remitente. Los valores posibles son: `focused`, `other`.|

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) actualizado en el cuerpo de la respuesta.
## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
En el ejemplo siguiente, se cambia la invalidación de la dirección SMTP randiw@adatum.onmicrosoft.com de `other` a `focused`.

<!-- {
  "blockType": "request",
  "name": "update_inferenceclassificationoverride"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/inferenceClassification/overrides/{id}
Content-type: application/json

{
  "classifyAs": "focused"
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
HTTP/1.1 200 OK
Content-type: application/json

{
  "classifyAs": "focused",
  "senderEmailAddress": {
    "name": "Randi Welch",
    "address": "randiw@adatum.onmicrosoft.com"
  },
  "id": "98f5bdef-576a-404d-a2ea-07a3cf34af4r"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update inferenceclassificationoverride",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->