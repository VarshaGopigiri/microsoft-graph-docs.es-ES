---
title: Creación de programa
description: En Azure AD tener acceso a la característica de revisiones, crear un nuevo objeto de programa.
localization_priority: Normal
ms.openlocfilehash: b982242bbdddb9769d64c9757d9041fddc215d53
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27844019"
---
# <a name="create-program"></a>Creación de programa

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

En la característica de [acceso revisa](../resources/accessreviews-root.md) Azure AD, cree un nuevo objeto de [programa](../resources/program.md) .
## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso                        | Permisos (de menos a más privilegiados)              |
|:--------------------------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa)     | `ProgramControl.ReadWrite.All`.  También debe ser el usuario iniciado en un rol de Active directory que le permita crear un programa. |
|Delegado (cuenta personal de Microsoft) | No admitida. |
|Aplicación                            | No admitida. |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /programs
```
## <a name="request-headers"></a>Encabezados de solicitud
| Nombre         | Tipo        | Descripción |
|:-------------|:------------|:------------|
| Autorización | string | Bearer \{token\}. Necesario. |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcionar una representación JSON de un objeto de [programa](../resources/program.md) .

La siguiente tabla muestran las propiedades que son necesarias cuando se crea un programa.

| Propiedad     | Tipo        | Description |
|:-------------|:------------|:------------|
| `displayName`               |`String`                              |  El nombre del programa.                   |
| `description`               |`String`                              |  La descripción del programa.           |


## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `201, Created` objeto de [programa](../resources/program.md) y el código de respuesta en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
En el cuerpo de la solicitud, proporcionar una representación JSON del objeto de [programa](../resources/program.md) .

<!-- {
  "blockType": "request",
  "name": "create_program_from_programs"
}-->
```http
POST https://graph.microsoft.com/beta/programs
Content-type: application/json

{
    "displayName": "testprogram3",
    "description": "test description"
}
```

##### <a name="response"></a>Respuesta
>**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.program"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
    "id": "7e59d237-2fb0-4e5d-b7bb-d4f9f9129213",
    "displayName": "testprogram3",
    "description": "test description"
}
```

## <a name="see-also"></a>Vea también

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Programas de lista](program-list.md) | colección de [programa](../resources/program.md)|  Obtener una colección de todos los programas.|
|[ProgramControls de lista de un programa](program-listcontrols.md) |     colección de [programControl](../resources/programcontrol.md)|    Obtener una colección de los controles de un programa.|
|[Programa de actualización](program-update.md) |  [programa](../resources/program.md)| Actualizar un programa.|
|[Crear programControl](programcontrol-create.md) |        [programControl](../resources/programcontrol.md)    |   Agregar un programControl a un programa.|

<!-- {
  "type": "#page.annotation",
  "description": "Create program",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
