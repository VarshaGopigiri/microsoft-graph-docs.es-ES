---
title: tipo de recurso macOSFirewallApplication
description: Representa una aplicación en la lista de aplicaciones de servidor de seguridad de Mac OS
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 536f2f596286f6b5457557f575ba018c65001bfe
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27835226"
---
# <a name="macosfirewallapplication-resource-type"></a>tipo de recurso macOSFirewallApplication

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Representa una aplicación en la lista de aplicaciones de servidor de seguridad de Mac OS
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|bundleId|Cadena|BundleId de la aplicación.|
|allowsIncomingConnections|Booleano|Si se permiten las conexiones entrantes.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.macOSFirewallApplication"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.macOSFirewallApplication",
  "bundleId": "String",
  "allowsIncomingConnections": true
}
```





