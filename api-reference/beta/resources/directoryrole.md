---
title: Tipo de recurso directoryRole
description: Representa un rol de Active directory de Azure AD. Las funciones de Active directory AD Azure también conocido como son *roles de administrador*. Para obtener más información acerca de las funciones de Active directory (Administrador), vea la asignación de roles de administrador en Azure AD. Con Microsoft Graph, puede asignar a usuarios a roles de Active directory para concederles los permisos de la función de destino. Para leer un rol de Active directory o actualizar a sus miembros, debe activarse en primer lugar en el inquilino. Sólo el rol de Active directory de administradores de la compañía se activa de forma predeterminada. Para activar otros roles de directorio disponible, envíe una solicitud POST con el identificador de la directoryRoleTemplate en el que se basa el rol de Active directory. Se hereda de directoryObject.
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: e6753369be070ab04419cab0c870aec7e96b1fb2
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27927747"
---
# <a name="directoryrole-resource-type"></a>Tipo de recurso directoryRole

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa un rol de Active directory de Azure AD. Las funciones de Active directory AD Azure también conocido como son *roles de administrador*. Para obtener más información acerca de las funciones de Active directory (Administrador), vea [asignación de roles de administrador en Azure AD](https://azure.microsoft.com/documentation/articles/active-directory-assign-admin-roles/). Con Microsoft Graph, puede asignar a usuarios a roles de Active directory para concederles los permisos de la función de destino. Para leer un rol de Active directory o actualizar a sus miembros, debe activarse en primer lugar en el inquilino. Sólo el rol de Active directory de administradores de la compañía se activa de forma predeterminada. Para activar otros roles de directorio disponible, envíe una solicitud POST con el identificador de la [directoryRoleTemplate](directoryroletemplate.md) en el que se basa el rol de Active directory. Se hereda de [directoryObject](directoryobject.md).

De forma predeterminada, las funciones de Active directory tengan un ámbito para que todo el inquilino.  Sin embargo, las funciones de Active directory (actualmente sólo el *Administrador de la cuenta de usuario* y *Administrador de departamento de soporte técnico*) también pueden aplicarse a [unidades administrativas](administrativeunit.md).

Este recurso admite:

- que use una [consulta delta](/graph/delta-query-overview) para realizar un seguimiento de los aumentos incrementales, las eliminaciones y las actualizaciones proporcionando una función [delta](../api/directoryrole-delta.md).

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Obtener directoryRole](../api/directoryrole-get.md) | [directoryRole](directoryrole.md) |Lea las propiedades y las relaciones del objeto directoryRole.|
|[List directoryRoles](../api/directoryrole-list.md) | Colección [directoryRole](directoryrole.md) | Enumera los roles de directorio que están activados en el inquilino. |
|[Agregar miembro](../api/directoryrole-post-members.md) |[directoryObject](directoryobject.md)| Agregue un usuario al rol de directorio; para ello, publique en la propiedad de navegación de miembros.|
|[Enumerar miembros](../api/directoryrole-list-members.md) |Colección [directoryObject](directoryobject.md)| Obtenga los usuarios que son miembros del rol de directorio de la propiedad de navegación de miembros.|
|[Quitar un miembro](../api/directoryrole-delete-member.md) |[directoryObject](directoryobject.md)| Elimine un usuario del rol de directorio.|
|[Miembros de la función con ámbito de lista](../api/directoryrole-list-members.md) |colección de [scopedRoleMembership](scopedrolemembership.md)| Lista de los miembros de este rol de Active directory que pertenecen al ámbito de [unidades administrativas](administrativeunit.md)a través de la colección de recursos de scopedRoleMembership.|
|[delta](../api/directoryrole-delta.md)|Colección directoryRole| Obtener cambios incrementales para funciones de Active directory. |

## <a name="properties"></a>Propiedades
| Propiedad   | Tipo |Descripción|
|:---------------|:--------|:----------|
|description|String|La descripción del rol de directorio. Solo lectura. |
|displayName|String|El nombre para mostrar del rol de directorio. Solo lectura. |
|id|String|El identificador único del rol de directorio. Hereda de [directoryObject](directoryobject.md). Clave, no admite valores NULL, solo lectura.|
|roleTemplateId|String| El **id** de la [directoryRoleTemplate](directoryroletemplate.md) en que se basa este rol. La propiedad debe especificarse al activar un rol de directorio en un inquilino con una operación POST. Una vez activado el rol de directorio, la propiedad es de solo lectura. |

## <a name="relationships"></a>Relaciones
| Relación | Tipo |Descripción|
|:---------------|:--------|:----------|
|members|Colección [directoryObject](directoryobject.md)|Usuarios que son miembros de este rol de directorio. Métodos HTTP: GET, POST, DELETE. Solo lectura. Admite valores NULL.|
|scopedMembers|colección de [scopedRoleMembership](scopedrolemembership.md)| Miembros de este rol de Active directory que pertenecen al ámbito de [unidades administrativas](administrativeunit.md). Solo lectura. Admite valores NULL.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "memberOf",
    "members",
    "ownedObjects",
    "owners"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.directoryRole"
}-->

```json
{
  "description": "string",
  "displayName": "string",
  "id": "string (identifier)",
  "roleTemplateId": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directoryRole resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
