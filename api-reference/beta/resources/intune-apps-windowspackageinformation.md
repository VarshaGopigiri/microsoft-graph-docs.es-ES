---
title: tipo de recurso windowsPackageInformation
description: Contiene las propiedades de la información del paquete para una línea de aplicación empresarial de Windows.
ms.openlocfilehash: a7676320d5aa2eeab1140e6cc631c4061d2c5d14
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087558"
---
# <a name="windowspackageinformation-resource-type"></a>tipo de recurso windowsPackageInformation

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades de la información del paquete para una línea de aplicación empresarial de Windows.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|applicableArchitecture|[windowsArchitecture](../resources/intune-apps-windowsarchitecture.md)|La arquitectura de Windows para la que se puede ejecutar esta aplicación en. Los valores posibles son: `none`, `x86`, `x64`, `arm` y `neutral`.|
|displayName|String|El nombre para mostrar.|
|identityName|String|Nombre de la identidad.|
|identityPublisher|String|El publicador de identidad.|
|identityResourceIdentifier|String|Identificador del recurso de identidad.|
|identityVersion|String|La versión de la identidad.|
|minimumSupportedOperatingSystem|[windowsMinimumOperatingSystem](../resources/intune-apps-windowsminimumoperatingsystem.md)|El valor para el sistema operativo mínimo aplicable.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsPackageInformation"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsPackageInformation",
  "applicableArchitecture": "String",
  "displayName": "String",
  "identityName": "String",
  "identityPublisher": "String",
  "identityResourceIdentifier": "String",
  "identityVersion": "String",
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.windowsMinimumOperatingSystem",
    "v8_0": true,
    "v8_1": true,
    "v10_0": true,
    "v10_1607": true,
    "v10_1703": true,
    "v10_1709": true,
    "v10_1803": true
  }
}
```





