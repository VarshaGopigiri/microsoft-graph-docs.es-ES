---
title: tipo de recurso macOSLobChildApp
description: Contiene las propiedades de la aplicación de LOB de Mac OS en un paquete de agrupación
author: tfitzmac
ms.openlocfilehash: e62305ea856d42847b49be306d20bde737152163
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27309873"
---
# <a name="macoslobchildapp-resource-type"></a>tipo de recurso macOSLobChildApp

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades de la aplicación de LOB de Mac OS en un paquete de agrupación
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|bundleId|String|Nombre de la identidad.|
|buildNumber|String|El número de compilación de línea de Mac OS de aplicación de negocio (LoB).|
|versionNumber|String|El número de versión de línea de Mac OS de aplicación de negocio (LoB).|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.macOSLobChildApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.macOSLobChildApp",
  "bundleId": "String",
  "buildNumber": "String",
  "versionNumber": "String"
}
```





