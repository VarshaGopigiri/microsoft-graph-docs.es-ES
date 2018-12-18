---
title: tipo de recurso mobileAppIntentAndStateDetail
description: La intención de aplicación móvil y el estado de instalación para un dispositivo dado.
author: tfitzmac
ms.openlocfilehash: 6a0a52d1cf8576778060c6f7b5e337e6e7a115e5
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27339224"
---
# <a name="mobileappintentandstatedetail-resource-type"></a>tipo de recurso mobileAppIntentAndStateDetail

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

La intención de aplicación móvil y el estado de instalación para un dispositivo dado.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|applicationId|cadena|Identificador de MobieApp.|
|displayName|String|Título de la aplicación importado o proporcionado por el administrador.|
|mobileAppIntent|[mobileAppIntent](../resources/intune-troubleshooting-mobileappintent.md)|Intención de aplicación móvil. Los valores posibles son: `available`, `notAvailable`, `requiredInstall`, `requiredUninstall`, `requiredAndAvailableInstall`, `availableInstallWithoutEnrollment` y `exclude`.|
|displayVersion|String|Versión legible humano de la aplicación|
|installState|[resultantAppState](../resources/intune-shared-resultantappstate.md)|El estado de instalación de la aplicación. Los valores posibles son: `installed`, `failed`, `notInstalled`, `uninstallFailed`, `pendingInstall`, `unknown` y `notApplicable`.|
|supportedDeviceTypes|colección de [mobileAppSupportedDeviceType](../resources/intune-troubleshooting-mobileappsupporteddevicetype.md)|Las plataformas compatibles para la aplicación.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mobileAppIntentAndStateDetail"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileAppIntentAndStateDetail",
  "applicationId": "String",
  "displayName": "String",
  "mobileAppIntent": "String",
  "displayVersion": "String",
  "installState": "String",
  "supportedDeviceTypes": [
    {
      "@odata.type": "microsoft.graph.mobileAppSupportedDeviceType",
      "type": "String",
      "minimumOperatingSystemVersion": "String",
      "maximumOperatingSystemVersion": "String"
    }
  ]
}
```





