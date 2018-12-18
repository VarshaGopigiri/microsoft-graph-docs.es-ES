---
title: Tipo de recurso configurationManagerClientEnabledFeatures
description: Características habilitadas del cliente de Configuration Manager
author: tfitzmac
ms.openlocfilehash: e0d704fddc084a455c83c5b55ea9b3911f3f232a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27343942"
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





