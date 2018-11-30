---
title: tipo de recurso teamsTabConfiguration (Open Type)
description: La configuración que determinan el contenido de una ficha.
ms.openlocfilehash: 4d04ca9128760ee6fed9c0fa704fa991384ac17a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028841"
---
# <a name="teamstabconfiguration-resource-type-open-type"></a>tipo de recurso teamsTabConfiguration (Open Type)



La configuración que determinan el contenido de una [ficha](teamstab.md). Cuando una ficha de forma interactiva se configura, esta información se establece mediante la aplicación de proveedor de la ficha.
Además de las propiedades que aparece a continuación, algunas aplicaciones de proveedor de la ficha especifican propiedades personalizadas adicionales.

## <a name="properties"></a>Propiedades

|Propiedad|Tipo|Descripción|
|-|-|-|
|  entityId   |   string |  Identificador de la entidad hospedada por el proveedor de la ficha.     |
|  contentUrl |   string |  Dirección URL utilizada para representar el contenido de la ficha en los equipos. Obligatorio.    |
|  removeUrl  |   string |  Dirección URL de los equipos cliente llamado cuando se quita una ficha mediante el cliente de los equipos.     |
|  websiteUrl |   string |  Dirección URL para mostrar el contenido de la ficha fuera de los equipos.     |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamsTabConfiguration"
}-->

```json
{
   "entityId": "string",
   "contentUrl": "string (HTTPS Url)",
   "websiteUrl": "string (HTTPS Url)",
   "removeUrl": "string (HTTPS Url)"  
}

```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "teamsTabConfiguration complex type (Open Type)",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
