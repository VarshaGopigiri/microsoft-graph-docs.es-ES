---
title: Crear grupo
description: 'Use esta API para crear un grupo como se especifica en el cuerpo de la solicitud. Puede crear uno de los tres tipos de grupos:'
author: dkershaw10
localization_priority: Priority
ms.prod: groups
ms.openlocfilehash: 2a3e0e20622db47d410b578249df94f3354e75ce
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27981549"
---
# <a name="create-group"></a>Crear grupo
Use esta API para crear un grupo como se especifica en el cuerpo de la solicitud. Puede crear uno de los tres tipos de grupos:

* Grupo de Office 365 (grupo unificado)
* Grupo dinámico
* Grupo de seguridad

> **Nota**: Aunque Microsoft Teams se basa en Grupos de Office 365, actualmente no puede crear un equipo mediante esta API. Puede usar las otras API de grupo para administrar un equipo que se ha creado en la interfaz de usuario de Microsoft Teams.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Group.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | No admitida.    |
|Aplicación | Group.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /groups
```

## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción|
|:---------------|:--------|:----------|
| Authorization  | string  | {token} de portador. Obligatorio. |

## <a name="request-body"></a>Cuerpo de la solicitud
En la siguiente tabla se muestra las propiedades del recurso de [grupo](../resources/group.md) para especificar cuando se crea un grupo. 

| Propiedad | Tipo | Descripción|
|:---------------|:--------|:----------|
| displayName | string | El nombre para mostrar en la libreta de direcciones del grupo. Obligatorio. |
| mailEnabled | boolean | Establézcalo en **true** para grupos habilitados para correo. Debe establecer en **true** si la creación de un grupo de Office 365. Debe establecer en **false** si crear dinámico o grupo de seguridad. Obligatorio. |
| mailNickname | string | El alias de correo del grupo. Obligatorio. |
| securityEnabled | boolean | Establecer en **true** para grupos de seguridad. Debe establecer en **true** si la creación de un grupo de seguridad o dinámicos. Debe establecer en **false** si la creación de un grupo de Office 365. Obligatorio. |
| owners | colección string | Esta propiedad representa los propietarios para el grupo en tiempo de creación. Opcional. |
| members | colección string | Esta propiedad representa a los miembros para el grupo en tiempo de creación. Opcional. |


Especificar la propiedad **groupTypes** si está creando un grupo de Office 365 o dinámico, como se indica a continuación.

### <a name="grouptypes-options"></a>Opciones de groupTypes

| Tipo de grupo | Propiedad **groupTypes** |
|:--------------|:------------------------|
| Office 365 (también conocido como grupo unificado)| "Unificado" |
| Dinámico | "DynamicMembership" |
| Seguridad | Sin establecer. |


>**Nota:** creación de un grupo de Office 365 mediante programación sin un contexto de usuario y sin especificar propietarios va a crear el grupo de forma anónima.  Al hacerlo, se puede producir en el sitio de SharePoint Online asociado, no se crean automáticamente hasta que más se lleva a cabo la acción manual.  

Especifique otras propiedades modificables según sea necesario para su grupo. Para más información, vea las propiedades del recurso [grupo](../resources/group.md).

## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [group](../resources/group.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
#### <a name="request-1"></a>Solicitud 1
La primera solicitud en el ejemplo crea un grupo de Office 365.
<!-- {
  "blockType": "request",
  "name": "create_group"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups
Content-type: application/json
Content-length: 244

{
  "description": "Self help community for library",
  "displayName": "Library Assist",
  "groupTypes": [
    "Unified"
  ],
  "mailEnabled": true,
  "mailNickname": "library",
  "securityEnabled": false
}
```

#### <a name="response-1"></a>Respuesta 1
Aquí tiene un ejemplo de la respuesta.
>**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.group"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 244

{
  "description": "Self help community for library",
  "displayName": "Library Assist",
  "groupTypes": [
    "Unified"
  ],
  "mail": "library@contoso.onmicrosoft.com",
  "mailEnabled": true,
  "mailNickname": "library",
  "securityEnabled": false
}
```

#### <a name="request-2"></a>Solicitud 2
La segunda solicitud de ejemplo crea un grupo de Office 365 con los propietarios de especificado.
<!-- {
  "blockType": "request"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups
Content-Type: application/json

{
  "description": "Group with owners",
  "displayName": "Group1",
  "groupTypes": [
    "Unified"
  ],
  "mailEnabled": true,
  "mailNickname": "group1",
  "securityEnabled": false,
  "owners@odata.bind": [
    "https://graph.microsoft.com/v1.0/users/26be1845-4119-4801-a799-aea79d09f1a2"
  ]
}
```

#### <a name="response-2"></a>Respuesta 2
El siguiente es un ejemplo de la respuesta correcta.
>**Nota:** el objeto de respuesta que se muestra aquí podría ser más cortos para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.group"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
    "description": "Group with owners",
    "displayName": "Group1",
    "groupTypes": [
        "Unified"
    ],
    "mail": "group1@contoso.onmicrosoft.com",
    "mailEnabled": true,
    "mailNickname": "group1",
    "securityEnabled": false
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create group",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
