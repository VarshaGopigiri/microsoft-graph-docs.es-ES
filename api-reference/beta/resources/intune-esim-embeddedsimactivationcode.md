---
title: tipo de recurso embeddedSIMActivationCode
description: El código de activación SIM incrustado como proporcionada por el operador móvil.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: af8bf020953dbc014f42aa6d363d3ca9e30db8a2
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27987408"
---
# <a name="embeddedsimactivationcode-resource-type"></a>tipo de recurso embeddedSIMActivationCode

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El código de activación SIM incrustado como proporcionada por el operador móvil.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|integratedCircuitCardIdentifier|Cadena|El identificador de tarjeta de circuito integrado (ICCID) para este de código de activación de SIM incrustado como proporcionado por el operador de telefonía móvil.
La entrada debe coincidir con la siguiente expresión regular: ' ^\[0-9\]{19}\[0-9\]?$ '.|
|matchingIdentifier|Cadena|MatchingIdentifier (MatchingID) tal como se especifica en la GSMA asociación SGP.22 RSP especificación técnica sección 4.1.
La entrada debe coincidir con la siguiente expresión regular: ' ^\[a-zA-Z0-9\-\]* $'.|
|smdpPlusServerAddress|Cadena|El nombre de dominio completo de la SM-DP + servidor tal como se especifica en la especificación técnica de GSM asociación SPG.22 RSP.
La entrada debe coincidir con la siguiente expresión regular: ' ^ (\[a-zA-Z0-9\]+(-\[a-zA-Z0-9\]+) *\.) +\[a-zA-Z\]{2,}$'.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.embeddedSIMActivationCode"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.embeddedSIMActivationCode",
  "integratedCircuitCardIdentifier": "String",
  "matchingIdentifier": "String",
  "smdpPlusServerAddress": "String"
}
```





