---
title: tipo de recurso windowsAppXAppAssignmentSettings
description: Contiene propiedades que se usan cuando se asigna una aplicación móvil de Windows AppX a un grupo.
author: tfitzmac
ms.openlocfilehash: 84103a91c3c670ef3da8a0ea2a2e38a95cff79a6
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27311623"
---
# <a name="windowsappxappassignmentsettings-resource-type"></a>tipo de recurso windowsAppXAppAssignmentSettings

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene propiedades que se usan cuando se asigna una aplicación móvil de Windows AppX a un grupo.

Hereda de [mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|useDeviceContext|Booleano|Si desea usar el contexto de ejecución de dispositivo para la aplicación móvil de Windows AppX.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsAppXAppAssignmentSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsAppXAppAssignmentSettings",
  "useDeviceContext": true
}
```





