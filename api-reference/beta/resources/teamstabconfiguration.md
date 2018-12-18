---
title: tipo de recurso teamsTabConfiguration (Open Type)
description: La configuración que determinan el contenido de una ficha.
author: nkramer
ms.openlocfilehash: 9abb4e9089da760825b29c4001b68881ab74d815
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27301186"
---
# <a name="teamstabconfiguration-resource-type-open-type"></a>tipo de recurso teamsTabConfiguration (Open Type)

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

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
