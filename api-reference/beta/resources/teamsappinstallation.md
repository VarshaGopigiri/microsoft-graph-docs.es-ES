---
title: tipo de recurso teamsAppInstallation
description: 'Un teamsApp instalado en un equipo. '
author: nkramer
localization_priority: Normal
ms.openlocfilehash: 5eca63cb3385fa03f8dffadff0482dc79a1dcfe3
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27871515"
---
# <a name="teamsappinstallation-resource-type"></a>tipo de recurso teamsAppInstallation

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

[TeamsApp](teamsapp.md) instalado en un [equipo](team.md). Cualquier bots que forman parte de la aplicación se convertirán en parte de cualquier equipo de a que la aplicación se agrega.

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Aplicaciones de lista](../api/teamsappinstallation-list.md) | [teamsAppInstallation](teamsapp.md) | Enumera aplicaciones instaladas en un equipo.|
|[Agregar aplicación](../api/teamsappinstallation-add.md) | [teamsAppInstallation](teamsapp.md) | Agrega (se instala) una aplicación a un equipo.|
|[Quitar aplicación](../api/teamsappinstallation-delete.md) | Ninguno | Quita (desinstala) una aplicación desde un equipo.|
|[Actualizar la aplicación](../api/teamsappinstallation-delete.md) | Ninguno | Actualizaciones a la versión más reciente de la aplicación.|

## <a name="properties"></a>Propiedades

| Propiedad            | Tipo     | Descripción |
|:------------------- |:-------- |:----------- |
| id                  | string   | Un identificador único (no el identificador de aplicación de los equipos). |

## <a name="relationships"></a>Relaciones

| Relación   | Tipo    | Description |
|:---------------|:--------|:----------|
|teamsApp|[teamsApp](teamsapp.md)| La aplicación que está instalada. |
|teamsAppDefinition|[teamsAppDefinition](teamsapp.md)| Los detalles de esta versión de la aplicación. |

## <a name="json-representation"></a>Representación JSON

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamsAppInstallation",
  "baseType": "microsoft.graph.entity"
}-->

```json
{
  "id": "string",
}
```

# <a name="see-also"></a>Vea también

- [teamsApp](teamsapp.md)
- [teamsAppDefinition](teamsappdefinition.md)
- [teamsTab](../resources/teamstab.md)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "teamsApp resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

