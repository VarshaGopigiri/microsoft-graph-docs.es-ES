---
title: Tipo de recurso directoryObject
description: Representa un objeto de Azure Active Directory. El tipo **directoryObject** es el tipo base para muchos otros tipos de entidad del directorio.
localization_priority: Priority
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 7f02687a8fc3b5b50f4e1e956da4bdc632ea389e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27952940"
---
# <a name="directoryobject-resource-type"></a>Tipo de recurso directoryObject

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa un objeto de Azure Active Directory. El tipo **directoryObject** es el tipo base para muchos otros tipos de entidad del directorio.

Este recurso admite:

- que use una [consulta delta](/graph/delta-query-overview) para realizar un seguimiento de los aumentos incrementales, las eliminaciones y las actualizaciones proporcionando una función [delta](../api/directoryobject-delta.md).

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Get directoryObject](../api/directoryobject-get.md) | [directoryObject](directoryobject.md) |Lee las propiedades de un objeto directory.|
|[Delete](../api/directoryobject-delete.md) | None |Elimina un objeto directory. |
|[checkMemberGroups](../api/directoryobject-checkmembergroups.md)|Colección string|Comprueba la pertenencia a una lista de grupos. La comprobación es transitiva.|
|[getMemberGroups](../api/directoryobject-getmembergroups.md)|Colección string|Devuelve todos los grupos de los que el usuario, grupo u objeto de directorio sea miembro. La comprobación es transitiva.|
|[getMemberObjects](../api/directoryobject-getmemberobjects.md)|Colección string| Devuelve todos los grupos y roles de directorio de los que el usuario, grupo u objeto de directorio sea miembro. La comprobación es transitiva. |
|[getByIds](../api/directoryobject-getbyids.md) | Colección [directoryObject](directoryobject.md) | Obtenga un conjunto de objetos de directorio basados en un conjunto de identificadores proporcionados. |
|[validateProperties](../api/directoryobject-validateproperties.md)|JSON| Validar el nombre para mostrar de un grupo de Office 365 o alias de correo cumplen con las políticas de nomenclatura. |
|[delta](../api/directoryobject-delta.md)|Colección directoryObject| Obtener cambios incrementales para los objetos de Active directory. Admite el filtrado por tipo de derivadas. |

## <a name="properties"></a>Propiedades

| Propiedad   | Tipo |Descripción|
|:---------------|:--------|:----------|
|id|Cadena|Un Guid que es el identificador único para el objeto; Por ejemplo, 12345678 9abc def0 1234 56789abcde12. Clave. No admite valores NULL. Solo lectura.|

## <a name="relationships"></a>Relaciones

Ninguno

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.directoryObject"
}-->

```json
{
  "id": "string (identifier)"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directoryObject resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
