---
title: Tipo de recurso configurationManagerClientEnabledFeatures
description: Características habilitadas del cliente de Configuration Manager
ms.openlocfilehash: 60d0e9e78bc4b641bb1f9ee0d61cc09744500424
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084507"
---
# <a name="configurationmanagerclientenabledfeatures-resource-type"></a>Tipo de recurso configurationManagerClientEnabledFeatures

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Características habilitadas del cliente de Configuration Manager
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|inventario|Booleano|Si el inventario se administra con Intune|
|modernApps|Booleano|Si la aplicación moderna se administra con Intune|
|resourceAccess|Booleano|Si el acceso a los recursos se administra con Intune|
|deviceConfiguration|Booleano|Si la configuración de dispositivos se administra con Intune|
|compliancePolicy|Booleano|Si la directiva de cumplimiento se administra con Intune|
|windowsUpdateForBusiness|Booleano|Si Windows Update para empresas se administra con Intune|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.configurationManagerClientEnabledFeatures"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.configurationManagerClientEnabledFeatures",
  "inventory": true,
  "modernApps": true,
  "resourceAccess": true,
  "deviceConfiguration": true,
  "compliancePolicy": true,
  "windowsUpdateForBusiness": true
}
```





