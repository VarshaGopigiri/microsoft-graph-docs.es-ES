---
title: tipo de recurso locationManagementCondition
description: Contiene la información para definir una condición de administración de la ubicación, un área de interés, para supervisar.
localization_priority: Normal
author: tfitzmac
ms.prod: intune
ms.openlocfilehash: 541cf74decad641f6dc7751945e1d0ffceee1366
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27922980"
---
# <a name="locationmanagementcondition-resource-type"></a>tipo de recurso locationManagementCondition

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene la información para definir una condición de administración de la ubicación, un área de interés, para supervisar.

Hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista locationManagementConditions](../api/intune-fencing-locationmanagementcondition-list.md)|colección de [locationManagementCondition](../resources/intune-fencing-locationmanagementcondition.md)|Propiedades de la lista y relaciones de los objetos [locationManagementCondition](../resources/intune-fencing-locationmanagementcondition.md) .|
|[Obtener locationManagementCondition](../api/intune-fencing-locationmanagementcondition-get.md)|[locationManagementCondition](../resources/intune-fencing-locationmanagementcondition.md)|Leer las propiedades y las relaciones del objeto [locationManagementCondition](../resources/intune-fencing-locationmanagementcondition.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Identificador único de la condición de administración. Valor asignado al crear generada por el sistema. Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)|
|uniqueName|Cadena|Nombre único para la condición de administración. Se usa en expresiones de condición de administración. Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)|
|displayName|Cadena|El nombre definido de administración de la condición de administración. Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)|
|descripción|Cadena|El administrador define la descripción de la condición de administración. Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)|
|createdDateTime|DateTimeOffset|La hora en que se creó la condición de administración. Servicio generado al lado. Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)|
|modifiedDateTime|DateTimeOffset|La hora en que se modificó por última vez la condición de administración. Se actualizó el lado de servicio. Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)|
|eTag|Cadena|ETag de la condición de administración. Se actualizó el lado de servicio. Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)|
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
  "@odata.type": "microsoft.graph.locationManagementCondition"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.locationManagementCondition",
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





