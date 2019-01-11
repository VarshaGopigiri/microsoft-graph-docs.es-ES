---
title: tipo de recurso officeUserCheckinSummary
description: Entidad que describe el inquilino protección de estadísticas.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: c2470b1e531f1b268d6797fe2692baf0031728b3
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27834026"
---
# <a name="officeusercheckinsummary-resource-type"></a>tipo de recurso officeUserCheckinSummary

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Entidad que describe el inquilino protección de estadísticas.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Description|
|:---|:---|:---|
|succeededUserCount|Int32|Total de usuario correcta comprobar ins para los últimos 3 meses.|
|failedUserCount|Int32|Total usuario erróneas comprobar ins para los últimos 3 meses.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.officeUserCheckinSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.officeUserCheckinSummary",
  "succeededUserCount": 1024,
  "failedUserCount": 1024
}
```



