---
title: Tipo de recurso windowsInformationProtectionAppLearningSummary
description: Entidad del resumen de aprendizaje de aplicación de Windows Information Protection.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 7175ec367bcf02843eff4dfff342c0e1da8120c3
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27952618"
---
# <a name="windowsinformationprotectionapplearningsummary-resource-type"></a>Tipo de recurso windowsInformationProtectionAppLearningSummary

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Entidad del resumen de aprendizaje de aplicación de Windows Information Protection.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar windowsInformationProtectionAppLearningSummaries](../api/intune-wip-windowsinformationprotectionapplearningsummary-list.md)|Colección [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md)|Enumere las propiedades y las relaciones de los objetos [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md).|
|[Obtener windowsInformationProtectionAppLearningSummary](../api/intune-wip-windowsinformationprotectionapplearningsummary-get.md)|[windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md)|Lea las propiedades y las relaciones del objeto [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md).|
|[Crear windowsInformationProtectionAppLearningSummary](../api/intune-wip-windowsinformationprotectionapplearningsummary-create.md)|[windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md)|Cree un objeto [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md).|
|[Eliminar windowsInformationProtectionAppLearningSummary](../api/intune-wip-windowsinformationprotectionapplearningsummary-delete.md)|Ninguna|Elimina un [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md).|
|[Actualizar windowsInformationProtectionAppLearningSummary](../api/intune-wip-windowsinformationprotectionapplearningsummary-update.md)|[windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md)|Actualice las propiedades de un objeto [windowsInformationProtectionAppLearningSummary](../resources/intune-wip-windowsinformationprotectionapplearningsummary.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Identificador único para WindowsInformationProtectionAppLearningSummary.|
|applicationName|String|Nombre de la aplicación|
|applicationType|[applicationType](../resources/intune-wip-applicationtype.md)|Tipo de aplicación. Los valores posibles son: `universal` y `desktop`.|
|deviceCount|Int32|Recuento de dispositivos|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsInformationProtectionAppLearningSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionAppLearningSummary",
  "id": "String (identifier)",
  "applicationName": "String",
  "applicationType": "String",
  "deviceCount": 1024
}
```



