---
title: tipo de recurso mobileAppTroubleshootingHistoryItem
description: Elemento de historial de contenidos en el evento de solución de problemas de aplicación móvil.
ms.openlocfilehash: 8fdeb522cd714f9265bc9f453fb5381bd925c481
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088573"
---
# <a name="mobileapptroubleshootinghistoryitem-resource-type"></a>tipo de recurso mobileAppTroubleshootingHistoryItem

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Elemento de historial de contenidos en el evento de solución de problemas de aplicación móvil.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|occurrenceDateTime|DateTimeOffset|Tiempo que se produjo el elemento de historial.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mobileAppTroubleshootingHistoryItem"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileAppTroubleshootingHistoryItem",
  "occurrenceDateTime": "String (timestamp)"
}
```





