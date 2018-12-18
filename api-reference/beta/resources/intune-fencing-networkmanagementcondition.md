---
title: tipo de recurso networkManagementCondition
description: Contiene la información para definir una condición de administración de la red.
author: tfitzmac
ms.openlocfilehash: d906520d30b78b0acdb1f33d7b4d7046d84c53e1
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27347596"
---
# <a name="networkmanagementcondition-resource-type"></a>tipo de recurso networkManagementCondition

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene la información para definir una condición de administración de la red.

Hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista networkManagementConditions](../api/intune-fencing-networkmanagementcondition-list.md)|colección de [networkManagementCondition](../resources/intune-fencing-networkmanagementcondition.md)|Propiedades de la lista y relaciones de los objetos [networkManagementCondition](../resources/intune-fencing-networkmanagementcondition.md) .|
|[Obtener networkManagementCondition](../api/intune-fencing-networkmanagementcondition-get.md)|[networkManagementCondition](../resources/intune-fencing-networkmanagementcondition.md)|Leer las propiedades y las relaciones del objeto [networkManagementCondition](../resources/intune-fencing-networkmanagementcondition.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Identificador único de la condición de administración. Valor asignado al crear generada por el sistema. Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)|
|uniqueName|String|Nombre único para la condición de administración. Se usa en expresiones de condición de administración. Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)|
|displayName|String|El nombre definido de administración de la condición de administración. Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)|
|descripción|String|El administrador define la descripción de la condición de administración. Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)|
|createdDateTime|DateTimeOffset|La hora en que se creó la condición de administración. Servicio generado al lado. Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)|
|modifiedDateTime|DateTimeOffset|La hora en que se modificó por última vez la condición de administración. Se actualizó el lado de servicio. Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)|
|eTag|String|ETag de la condición de administración. Se actualizó el lado de servicio. Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)|
|applicablePlatforms|colección de [devicePlatformType](../resources/intune-shared-deviceplatformtype.md)|Las plataformas aplicables para esta condición de administración. Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|managementConditionStatements|colección de [managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md)|Las instrucciones de condición de administración asociadas a la condición de administración. Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.networkManagementCondition"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.networkManagementCondition",
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





