---
title: tipo de recurso win32LobAppMsiInformation
description: Contiene propiedades de la aplicación MSI para una aplicación de Win32.
author: tfitzmac
ms.openlocfilehash: 1753df68ab1f4b0e1649c16a4a7fa0ad49941bf9
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27326141"
---
# <a name="win32lobappmsiinformation-resource-type"></a>tipo de recurso win32LobAppMsiInformation

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene propiedades de la aplicación MSI para una aplicación de Win32.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|productCode|String|El código de producto MSI.|
|productVersion|String|La versión del producto MSI.|
|upgradeCode|String|El código de actualización MSI.|
|requiresReboot|Boolean|Si la aplicación MSI requiere que el equipo que reiniciar para completar la instalación.|
|packageType|[win32LobAppMsiPackageType](../resources/intune-apps-win32lobappmsipackagetype.md)|El tipo de paquete MSI. Los valores posibles son: `perMachine`, `perUser` y `dualPurpose`.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.win32LobAppMsiInformation"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.win32LobAppMsiInformation",
  "productCode": "String",
  "productVersion": "String",
  "upgradeCode": "String",
  "requiresReboot": true,
  "packageType": "String"
}
```





