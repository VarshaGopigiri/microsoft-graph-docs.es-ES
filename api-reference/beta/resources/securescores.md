---
title: tipo de recurso secureScores
description: 'parte superior = n, donde n = número de días de datos que desea recuperar. '
localization_priority: Normal
ms.openlocfilehash: 332a9656d8237bb07d5c7739b666e09539cf984f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27828738"
---
# <a name="securescores-resource-type"></a>tipo de recurso secureScores

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa la puntuación de seguro de un inquilino por día de los resultados de datos, en el nivel de inquilino y control. De forma predeterminada, se mantiene 90 días de datos. Estos datos se ordenan por **createdDateTime**, de más reciente a más próxima. Esto le permitirá a las respuestas de la página mediante el uso de $top = n, donde n = número de días de datos que desea recuperar. 


## <a name="methods"></a>Métodos

| Método   | Tipo de valor devuelto|Descripción|
|:---------------|:--------|:----------|
|[Lista secureScores](../api/securescores-list.md) | [secureScores](securescores.md) |Lea las propiedades y los metadatos de un objeto secureScores.|


## <a name="properties"></a>Propiedades
Que contiene propiedades de tipo de entidad de la seguridad del inquilino puntuación (datos de instantánea diaria).

|Propiedad |Tipo |Description |
|:--|:--|:--|
|   azureTenantId   |   Cadena  |   Identificador de cadena GUID para el inquilino.  |
|   createdDateTime |   DateTimeOffset  |   La fecha cuando se crea la entidad.  |
|   id  |   Cadena  |   Combinación de azureTenantId_createdDateTime.   |
|   licensedUserCount   |   Int32   |   Con una licencia de recuento de usuarios del inquilino determinado.    |
|   activeUserCount |   Int32   |   Recuento de usuario activo del inquilino determinado.  |
|   currentScore    |   Doble  |   Puntuación actual del inquilino alcanzado en la fecha especificada.    |
|   maxScore |  Doble  |   Inquilino máxima puntuación posible en la fecha especificada.    |
|   enabledServices |   Colección String   |   Servicios proporcionados por Microsoft para el inquilino (por ejemplo, Exchange online, Skype, Sharepoint).   |
|   averageComparativeScores |  colección de [averageComparativeScore](averagecomparativescore.md)    |Promedio de la puntuación por distintos ámbitos (por ejemplo, promedio según el sector, promedio por asiento) y categoría de control (identidad, datos, dispositivos, aplicaciones, infraestructura) dentro del ámbito. |
|   controlScores | colección de [controlScore](controlscore.md)  |   Contiene las puntuaciones del inquilino para un conjunto de controles.   |


## <a name="relationships"></a>Relaciones

Ninguna.

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.secureScores"
}-->

```json
{
"id": "String",
"azureTenantId": "Guid",
"createdDate": "DateTimeOffset",
"licensedUserCount": "Int32",
"activeUserCount": "Int32",
"currentScore": "Int32",
"maxScore": "Int32",
"averageScore": "Double",
"enabledServices": "Collection(string)",
"averageComparativeScores": "Collection(microsoft.graph.SecureScore.averageComparativeScores)",
"controlScores": "Collection(microsoft.graph.SecureScore.controlScores)",
}

```


<!-- {
  "type": "#page.annotation",
  "description": "secureScores resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
