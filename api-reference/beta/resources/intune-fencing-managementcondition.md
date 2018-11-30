---
title: tipo de recurso managementCondition
description: Condiciones de administración son eventos que se pueden desencadenar dinámicamente como ubican-barreras, límites de tiempo y límites de la red.
ms.openlocfilehash: 3c2bc1d7594e61642b96398bfb55d6aa38f3283d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085177"
---
# <a name="managementcondition-resource-type"></a>tipo de recurso managementCondition

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Condiciones de administración son eventos que se pueden desencadenar dinámicamente como ubican-barreras, límites de tiempo y límites de la red.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista managementConditions](../api/intune-fencing-managementcondition-list.md)|colección de [managementCondition](../resources/intune-fencing-managementcondition.md)|Propiedades de la lista y relaciones de los objetos [managementCondition](../resources/intune-fencing-managementcondition.md) .|
|[Obtener managementCondition](../api/intune-fencing-managementcondition-get.md)|[managementCondition](../resources/intune-fencing-managementcondition.md)|Leer las propiedades y las relaciones del objeto [managementCondition](../resources/intune-fencing-managementcondition.md) .|
|[getManagementConditionsForPlatform (función)](../api/intune-fencing-managementcondition-getmanagementconditionsforplatform.md)|colección de [managementCondition](../resources/intune-fencing-managementcondition.md)|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Identificador único de la condición de administración. Valor asignado al crear generada por el sistema.|
|uniqueName|String|Nombre único para la condición de administración. Se usa en expresiones de condición de administración.|
|displayName|String|El nombre definido de administración de la condición de administración.|
|descripción|String|El administrador define la descripción de la condición de administración.|
|createdDateTime|DateTimeOffset|La hora en que se creó la condición de administración. Servicio generado al lado.|
|modifiedDateTime|DateTimeOffset|La hora en que se modificó por última vez la condición de administración. Se actualizó el lado de servicio.|
|eTag|String|ETag de la condición de administración. Se actualizó el lado de servicio.|
|applicablePlatforms|colección de [devicePlatformType](../resources/intune-shared-deviceplatformtype.md)|Las plataformas aplicables para esta condición de administración.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|managementConditionStatements|colección de [managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md)|Las instrucciones de condición de administración asociadas a la condición de administración.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managementCondition"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managementCondition",
  "id": "String (identifier)",
  "uniqueName": "String",
  "displayName": "String",
  "description": "String",
  "createdDateTime": "String (timestamp)",
  "modifiedDateTime": "String (timestamp)",
  "eTag": "String",
  "applicablePlatforms": [
    "String"
  ]
}
```





