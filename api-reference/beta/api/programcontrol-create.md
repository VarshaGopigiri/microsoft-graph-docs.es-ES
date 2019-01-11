---
title: Crear programControl
description: En Azure AD tener acceso a la característica de revisiones, crear un nuevo objeto programControl.  Esto vincula una revisión de acceso a un programa.
localization_priority: Normal
ms.openlocfilehash: 4dfbb76244a41867b8a57faa42f63dc728f59136
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27851537"
---
# <a name="create-programcontrol"></a>Crear programControl

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

En la característica de [acceso revisa](../resources/accessreviews-root.md) Azure AD, cree un nuevo objeto [programControl](../resources/programcontrol.md) .  Esto vincula una revisión de acceso a un programa.

Antes de realizar esta solicitud, el llamador debe tener anteriormente

 - [crea un programa](program-create.md) o [recuperar un programa](program-list.md), para que el valor de `programId` para incluir en la solicitud,
 - [crea una revisión de acceso](accessreview-create.md) o [recuperar una revisión de acceso](accessreview-get.md), para que el valor de `controlId` para incluir en la solicitud, y
 - [recupera la lista de tipos de control de programa](programcontroltype-list.md), para que el valor de `controlTypeId` para incluir en la solicitud.


## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso                        | Permisos (de menos a más privilegiados)              |
|:--------------------------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa)     | `ProgramControl.ReadWrite.All`.  El usuario iniciado también debe estar en un rol de Active directory que le permita crear un programControl. |
|Delegado (cuenta personal de Microsoft) | No admitida. |
|Aplicación                            | No admitida. |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /programControls
```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre         | Tipo        | Descripción |
|:-------------|:------------|:------------|
| Autorización | string | Bearer \{token\}. Necesario. |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcionar una representación JSON de un objeto [programControl](../resources/programcontrol.md) .

La siguiente tabla muestran las propiedades que son necesarias cuando se crea un control de programa.

| Propiedad     | Tipo        | Description |
|:-------------|:------------|:------------|
| `programId`              |`String`                | El programId del programa de este control se va a convertirse en una parte de.                             |
| `controlId`              |`String`                | ControlId del control, en particular, el identificador de una revisión de access.                                                |
| `controlTypeId`          |`String`                | El programControlType identifica el tipo de control de programa: por ejemplo, se revisa un control de vinculación para acceso de invitado. |

## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `201, Created` código de respuesta y un objeto [programControl](../resources/programcontrol.md) en el cuerpo de la respuesta.


## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
En el cuerpo de la solicitud, proporcionar una representación JSON del objeto [programControl](../resources/programcontrol.md) .

<!-- {
  "blockType": "request",
  "name": "create_programControl_from_programControls"
}-->
```http
POST https://graph.microsoft.com/beta/programControls
Content-type: application/json

{
    "controlId": "7e59d237-2fb0-4e5d-b7bb-d4f9f9129213",
    "controlTypeId": "6e4f3d20-c5c3-407f-9695-8460952bcc68",
    "programId": "7e59d237-2fb0-4e5d-b7bb-d4f9f9129213"
}
```

##### <a name="response"></a>Respuesta
>**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.programControl"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
  "id": "63b2302c-7e62-43b7-aefb-063ba5bdb853",
  "controlId": "7e59d237-2fb0-4e5d-b7bb-d4f9f9129213",
  "programId": "7e59d237-2fb0-4e5d-b7bb-d4f9f9129213",
  "controlTypeId": "6e4f3d20-c5c3-407f-9695-8460952bcc68",
  "displayName": "test",
  "status": "Active",
  "createdDateTime": "2018-05-18T20:26:05.2976279Z"
}
```

## <a name="see-also"></a>Vea también

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Lista programControlTypes](../api/programcontroltype-list.md) | colección de [programControlType](../resources/programcontroltype.md)| Lista de tipos de control de programa. |


<!-- {
  "type": "#page.annotation",
  "description": "Create programControl",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
