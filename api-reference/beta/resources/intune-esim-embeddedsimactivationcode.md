---
title: tipo de recurso embeddedSIMActivationCode
description: El código de activación SIM incrustado como proporcionada por el operador móvil.
author: tfitzmac
ms.openlocfilehash: 4e768a4047b8ddc785b545d3b850128a8e44f256
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27311791"
---
# <a name="embeddedsimactivationcode-resource-type"></a>tipo de recurso embeddedSIMActivationCode

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El código de activación SIM incrustado como proporcionada por el operador móvil.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|integratedCircuitCardIdentifier|String|El identificador de tarjeta de circuito integrado (ICCID) para este de código de activación de SIM incrustado como proporcionado por el operador de telefonía móvil.
La entrada debe coincidir con la siguiente expresión regular: ' ^\[0-9\]{19}\[0-9\]?$ '.|
|matchingIdentifier|String|MatchingIdentifier (MatchingID) tal como se especifica en la GSMA asociación SGP.22 RSP especificación técnica sección 4.1.
La entrada debe coincidir con la siguiente expresión regular: ' ^\[a-zA-Z0-9\-\]* $'.|
|smdpPlusServerAddress|String|El nombre de dominio completo de la SM-DP + servidor tal como se especifica en la especificación técnica de GSM asociación SPG.22 RSP.
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





