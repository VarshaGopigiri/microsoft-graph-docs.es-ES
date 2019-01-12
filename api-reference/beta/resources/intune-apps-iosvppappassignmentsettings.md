---
title: Tipo de recurso iosVppAppAssignmentSettings
description: Contiene las propiedades que se usan para asignar a un grupo una aplicación móvil de VPP para iOS.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: b62a44e34ca19b80c35062c884c00fd5ceeaeb38
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27919263"
---
# <a name="iosvppappassignmentsettings-resource-type"></a>Tipo de recurso iosVppAppAssignmentSettings

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades que se usan para asignar a un grupo una aplicación móvil de VPP para iOS.

Hereda de [mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|useDeviceLicensing|Booleano|Si se deben usar o no las licencias de dispositivo.|
|vpnConfigurationId|cadena|El identificador de configuración de VPN que se aplicará a esta aplicación.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosVppAppAssignmentSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosVppAppAssignmentSettings",
  "useDeviceLicensing": true,
  "vpnConfigurationId": "String"
}
```





