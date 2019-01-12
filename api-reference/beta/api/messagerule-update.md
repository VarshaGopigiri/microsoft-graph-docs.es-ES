---
title: Actualizar regla
description: Cambie las propiedades modificables en un objeto messageRule y guarde los cambios.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: ce58fd5c3a1156273cec9c62f322d4fe198d03f7
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27919918"
---
# <a name="update-rule"></a>Actualizar regla

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Cambie las propiedades modificables en un objeto [messageRule](../resources/messagerule.md) y guarde los cambios.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | MailboxSettings.ReadWrite    |
|Delegado (cuenta personal de Microsoft) | MailboxSettings.ReadWrite    |
|Aplicación | MailboxSettings.ReadWrite |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/mailFolders/inbox/messagerules/{id}
PATCH /users/{id | userPrincipalName}/mailFolders/inbox/messagerules/{id}
```
## <a name="optional-request-headers"></a>Encabezados de solicitud opcionales
| Nombre       | Descripción|
|:-----------|:-----------|
| Authorization  | {token} de portador. Obligatorio. |


## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.

| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
| actions | [messageRuleActions](../resources/messageruleactions.md) | Acciones que se van a realizar en un mensaje cuando se cumplan las condiciones correspondientes. |
| conditions | [messageRulePredicates](../resources/messagerulepredicates.md) | Condiciones que, cuando se cumplan, activarán las acciones correspondientes a esa regla. |
| displayName | String | Nombre para mostrar de la regla. |
| exceptions | [messageRulePredicates](../resources/messagerulepredicates.md) | Condiciones de excepción de la regla. |
| isEnabled | Boolean | Indica si la regla está habilitada para que se aplique a los mensajes. |
| isReadOnly | Boolean | Indica si la regla es de solo lectura y la API de REST de reglas no la puede modificar ni eliminar. |
| sequence | Int32 | Indica el orden en que se ejecuta la regla entre otras reglas. |


## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [messageRule](../resources/messagerule.md) actualizado en el cuerpo de la respuesta.
## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
En el ejemplo siguiente se cambia el nombre de la regla y las acciones que se realizan para esa regla en el [ejemplo](messagerule-get.md#example) de [Obtener regla](messagerule-get.md), desde reenviarla a una dirección hasta marcar su importancia como alta. 
<!-- {
  "blockType": "request",
  "name": "update_messagerule"
}-->
```http
PATCH https://graph.microsoft.com/beta/me/mailfolders/inbox/messagerules('AQAAAJ5dZqA=')

Content-type: application/json

{
    "displayName": "Important from partner",
    "actions": {
        "markImportance": "high"
     }
} 
```
##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.messageRule"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#Me/mailFolders('inbox')/messageRules/$entity",
  "id":"AQAAAJ5dZqA=",
  "displayName":"Important from partner",
  "sequence":2,
  "isEnabled":true,
  "hasError":false,
  "isReadOnly":false,
  "conditions":{
    "senderContains":[
      "ADELE"
    ]
  },
  "actions":{
    "markImportance": "high"
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update rule",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
