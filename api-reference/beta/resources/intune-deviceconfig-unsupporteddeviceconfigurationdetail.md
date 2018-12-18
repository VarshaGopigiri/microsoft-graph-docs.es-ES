---
title: tipo de recurso unsupportedDeviceConfigurationDetail
description: Una descripción de por qué una entidad no es compatible.
author: tfitzmac
ms.openlocfilehash: 4cccf49366a803e5f964605a4dc4ba7f56707823
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27344054"
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





