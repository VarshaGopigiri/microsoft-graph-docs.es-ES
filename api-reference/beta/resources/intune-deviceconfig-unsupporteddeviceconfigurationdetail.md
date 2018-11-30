---
title: tipo de recurso unsupportedDeviceConfigurationDetail
description: Una descripción de por qué una entidad no es compatible.
ms.openlocfilehash: d64d6aedf5da0f3cd79e2582d84fa4f19ea7ccfa
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084722"
---
# <a name="unsupporteddeviceconfigurationdetail-resource-type"></a>tipo de recurso unsupportedDeviceConfigurationDetail

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Una descripción de por qué una entidad no es compatible.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|message|String|Un mensaje que explica por qué una entidad no es compatible.|
|propertyName|String|Si el mensaje está relacionado con una propiedad concreta en la entidad original y, a continuación, el nombre de esa propiedad.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.unsupportedDeviceConfigurationDetail"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.unsupportedDeviceConfigurationDetail",
  "message": "String",
  "propertyName": "String"
}
```





