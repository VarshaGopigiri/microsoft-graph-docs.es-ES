---
title: tipo de recurso chatMessageMention
description: 'Representa una mención en una entidad de chatMessage. Puede ser la mención a un usuario, equipo, bot o canal. '
localization_priority: Normal
ms.openlocfilehash: 7b24d2af6f61f3da69480557e1c5b5f32c009c25
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27876142"
---
# <a name="chatmessagemention-resource-type"></a>tipo de recurso chatMessageMention

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa una mención en una entidad de [chatMessage](chatmessage.md) . Puede ser la mención a un usuario, equipo, bot o canal. 

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|id|string|Identificador de la entidad que se menciona|
|mentionText|string|Cadena que se utiliza para representar la mención ej: nombre de usuario para mostrar, nombre de equipo etcetera|
|mencionado|[identitySet](identityset.md)|El usuario que se ha mencionado|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.chatMessageMention"
}-->

```json
{
  "id": "string (identifier)",
  "mentionText": "string",
  "mentioned": "microsoft.graph.identitySet"
 }

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "chat mention resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
