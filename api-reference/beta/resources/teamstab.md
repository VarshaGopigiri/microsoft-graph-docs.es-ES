---
title: tipo de recurso teamsTab
description: 'Una teamsTab es una ficha que ha anclado (adjunto) a un canal dentro de un equipo. '
localization_priority: Normal
author: nkramer
ms.prod: microsoft-teams
ms.openlocfilehash: 3c5cf5ef33f53cfaca7189df24e5dfd880a77241
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27947151"
---
# <a name="teamstab-resource-type"></a>tipo de recurso teamsTab

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Una teamsTab es una [ficha](../resources/teamstab.md) que ha anclado (adjunto) a un [canal](channel.md) dentro de un [equipo](team.md). 

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Fichas de lista](../api/teamstab-list.md) | [teamsTab](teamstab.md) | Las fichas de listas anclado a un canal.|
|[Obtener la ficha](../api/teamstab-get.md) | [teamsTab](teamstab.md) | Lee una ficha anclada a un canal.|
|[Agregar ficha](../api/teamstab-add.md) | [teamsTab](teamstab.md) | (PIN) se agrega una ficha a un canal.|
|[Quitar la ficha](../api/teamstab-delete.md) | Ninguno | Quita (libera) una ficha de un canal.|
|[Ficha de actualización](../api/teamstab-update.md) | [teamsTab](teamstab.md) | Actualiza las propiedades de la ficha.|


## <a name="properties"></a>Propiedades

|Propiedad|Tipo|Descripción|
|:---------------|:--------|:----------|
|  id              |   string                  |  Identificador que identifica de forma exclusiva una instancia específica de una ficha de canal lectura sólo.     |
|  displayName            |   string                  |  Nombre de la ficha.     |
|  name            |   string                  |  (Obsoleto) Nombre de la ficha.     |
|  teamsAppId           |   string             |  Identificador de la definición de aplicación de la ficha. No se puede cambiar este valor después de la creación de la ficha.     |
|  sortOrderIndex  |   int                     |  Índice del orden utilizado para la ordenación de las fichas.     |
|  webUrl          |   string                  |  Dirección url del vínculo profundo de la instancia de ficha. Solo lectura.     |
|  configuration        |   [teamsTabConfiguration](teamstabconfiguration.md) |  Contenedor de configuración personalizada que se aplican a una ficha. La ficha se considera configurado sólo una vez que se establece esta propiedad.     |

## <a name="relationships"></a>Relaciones

| Relación | Tipo   | Descripción |
|:---------------|:--------|:----------|
|teamsApp|[teamsApp](teamsapp.md) | La aplicación que está vinculada a la ficha. |

## <a name="json-representation"></a>Representación JSON

Esta es una representación JSON del recurso.


<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.teamsTab"
}-->

```json
{  
  "id": "string",
  "displayName": "string",
  "teamsAppId": "string",
  "sortOrderIndex": "string",
  "webUrl": "string",
  "configuration" : "teamsTabConfiguration"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "teamsTab resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

## <a name="see-also"></a>Vea también

[Configuración de los tipos de ficha integrada](/graph/teams-configuring-builtin-tabs)
