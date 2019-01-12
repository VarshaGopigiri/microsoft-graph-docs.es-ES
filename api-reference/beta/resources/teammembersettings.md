---
title: tipo de recurso teamMemberSettings
description: Configuración para configurar si los miembros pueden realizar determinadas acciones, por ejemplo, creación de canales y agrega bots, en el equipo.
localization_priority: Normal
author: nkramer
ms.prod: microsoft-teams
ms.openlocfilehash: 3854481e89f04fa727b77c6b4f8699c62a16d739
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27978252"
---
# <a name="teammembersettings-resource-type"></a>tipo de recurso teamMemberSettings

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Configuración para configurar si los miembros pueden realizar determinadas acciones, por ejemplo, creación de canales y agrega bots, en el [equipo](team.md).

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|allowCreateUpdateChannels|Booleano|Si se establece a miembros es true, puede agregar y actualizar los canales.|
|allowDeleteChannels|Booleano|Si se establece en true, miembros puede eliminar canales.|
|allowAddRemoveApps|Booleano|Si se establece a miembros es true, puede agregar y quitar aplicaciones.|
|allowCreateUpdateRemoveTabs|Booleano|Si se establece en true, miembros puede agregar, actualizar y quitar las fichas. |
|allowCreateUpdateRemoveConnectors|Booleano|Si se establece en true, miembros puede agregar, actualizar y quitar conectores.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamMemberSettings"
}-->

```json
{
  "allowCreateUpdateChannels": true,
  "allowDeleteChannels": true,
  "allowAddRemoveApps": true,
  "allowCreateUpdateRemoveTabs": true,
  "allowCreateUpdateRemoveConnectors": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "team's memberSettings resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
