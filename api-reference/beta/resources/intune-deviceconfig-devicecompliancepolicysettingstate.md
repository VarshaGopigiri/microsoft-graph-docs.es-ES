---
title: Tipo de recurso deviceCompliancePolicySettingState
description: Estados de configuración de directivas de cumplimiento del dispositivo para un dispositivo determinado.
author: tfitzmac
ms.openlocfilehash: fbad84edffaeb3abdff0c00fdd55c1451d23a721
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27327961"
---
# <a name="devicecompliancepolicysettingstate-resource-type"></a>Tipo de recurso deviceCompliancePolicySettingState

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Estados de configuración de directivas de cumplimiento del dispositivo para un dispositivo determinado.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|ajustes|Cadena|La configuración que se está notificando|
|settingName|Cadena|Nombre descriptivo de la configuración de usuario o localizada que se está notificando|
|instanceDisplayName|Cadena|Nombre de la instancia de configuración que se está notificando.|
|estado|[complianceStatus](../resources/intune-shared-compliancestatus.md)|El estado de cumplimiento de la configuración. Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.|
|errorCode|Int64|Código de error de la configuración|
|errorDescription|Cadena|Descripción del error|
|userId|Cadena|UserId|
|userName|Cadena|UserName|
|userEmail|Cadena|UserEmail|
|userPrincipalName|String|UserPrincipalName.|
|orígenes|Colección [settingSource](../resources/intune-deviceconfig-settingsource.md)|Directivas colaboradoras|
|currentValue|Cadena|Valor actual de la configuración en el dispositivo|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceCompliancePolicySettingState"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceCompliancePolicySettingState",
  "setting": "String",
  "settingName": "String",
  "instanceDisplayName": "String",
  "state": "String",
  "errorCode": 1024,
  "errorDescription": "String",
  "userId": "String",
  "userName": "String",
  "userEmail": "String",
  "userPrincipalName": "String",
  "sources": [
    {
      "@odata.type": "microsoft.graph.settingSource",
      "id": "String",
      "displayName": "String"
    }
  ],
  "currentValue": "String"
}
```





