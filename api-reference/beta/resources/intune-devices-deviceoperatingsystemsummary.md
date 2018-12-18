---
title: Tipo de recurso deviceOperatingSystemSummary
description: Resumen de sistemas operativos de dispositivos.
author: tfitzmac
ms.openlocfilehash: 8dd3bf85a75d5acf6ae4bb0cecb8fd360c4e0459
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27341863"
---
# <a name="deviceoperatingsystemsummary-resource-type"></a>Tipo de recurso deviceOperatingSystemSummary

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Resumen de sistemas operativos de dispositivos.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|androidCount|Int32|Número del recuento de dispositivos Android.|
|iosCount|Int32|Número del recuento de dispositivos iOS.|
|macOSCount|Int32|Número del recuento de dispositivos Mac OS X.|
|windowsMobileCount|Int32|Número del recuento de dispositivos móviles Windows.|
|windowsCount|Int32|Número del recuento de dispositivos Windows.|
|unknownCount|Int32|Número del recuento de dispositivos desconocidos.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceOperatingSystemSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceOperatingSystemSummary",
  "androidCount": 1024,
  "iosCount": 1024,
  "macOSCount": 1024,
  "windowsMobileCount": 1024,
  "windowsCount": 1024,
  "unknownCount": 1024
}
```





