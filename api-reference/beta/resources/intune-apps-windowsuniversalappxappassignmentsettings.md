---
title: tipo de recurso windowsUniversalAppXAppAssignmentSettings
description: Contiene propiedades que se usan cuando se asigna una aplicación móvil AppX universales de Windows a un grupo.
author: tfitzmac
ms.openlocfilehash: 46f54acb1116c177e330bda868b975bdf361fe5c
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27329228"
---
# <a name="windowsuniversalappxappassignmentsettings-resource-type"></a>tipo de recurso windowsUniversalAppXAppAssignmentSettings

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene propiedades que se usan cuando se asigna una aplicación móvil AppX universales de Windows a un grupo.

Hereda de [mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|useDeviceContext|Booleano|Si desea usar el contexto de ejecución de dispositivo para aplicación móvil AppX universales de Windows.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsUniversalAppXAppAssignmentSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsUniversalAppXAppAssignmentSettings",
  "useDeviceContext": true
}
```





