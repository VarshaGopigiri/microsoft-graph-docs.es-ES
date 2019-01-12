---
title: tipo de recurso officeConfigurationGroupAssignmentTarget
description: Configuración de cliente de Office AAD grupo de destino de la asignación.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 9d59a6adc5478d619187e5414ac92170cbdedd49
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27926382"
---
# <a name="officeconfigurationgroupassignmenttarget-resource-type"></a>tipo de recurso officeConfigurationGroupAssignmentTarget

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Configuración de cliente de Office AAD grupo de destino de la asignación.

Hereda de [officeConfigurationAssignmentTarget](../resources/intune-cirrus-officeconfigurationassignmenttarget.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|groupId|Cadena|El identificador del grupo AAD, nuestro destino son para la configuración del dispositivo.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.officeConfigurationGroupAssignmentTarget"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.officeConfigurationGroupAssignmentTarget",
  "groupId": "String"
}
```



