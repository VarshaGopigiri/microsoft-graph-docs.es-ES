---
title: tipo de recurso circularGeofenceManagementCondition
description: Contiene la información para definir una condición de administración ubican-barrera circular, un área de interés, para supervisar.
localization_priority: Normal
author: tfitzmac
ms.prod: intune
ms.openlocfilehash: bd7ae4b50ab7ec1497544fe8247f5d6d7e80e083
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27925367"
---
# <a name="circulargeofencemanagementcondition-resource-type"></a>tipo de recurso circularGeofenceManagementCondition

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene la información para definir una condición de administración ubican-barrera circular, un área de interés, para supervisar.

Hereda de [locationManagementCondition](../resources/intune-fencing-locationmanagementcondition.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista circularGeofenceManagementConditions](../api/intune-fencing-circulargeofencemanagementcondition-list.md)|colección de [circularGeofenceManagementCondition](../resources/intune-fencing-circulargeofencemanagementcondition.md)|Propiedades de la lista y relaciones de los objetos [circularGeofenceManagementCondition](../resources/intune-fencing-circulargeofencemanagementcondition.md) .|
|[Obtener circularGeofenceManagementCondition](../api/intune-fencing-circulargeofencemanagementcondition-get.md)|[circularGeofenceManagementCondition](../resources/intune-fencing-circulargeofencemanagementcondition.md)|Leer las propiedades y las relaciones del objeto [circularGeofenceManagementCondition](../resources/intune-fencing-circulargeofencemanagementcondition.md) .|
|[Crear circularGeofenceManagementCondition](../api/intune-fencing-circulargeofencemanagementcondition-create.md)|[circularGeofenceManagementCondition](../resources/intune-fencing-circulargeofencemanagementcondition.md)|Crear un nuevo objeto [circularGeofenceManagementCondition](../resources/intune-fencing-circulargeofencemanagementcondition.md) .|
|[Eliminar circularGeofenceManagementCondition](../api/intune-fencing-circulargeofencemanagementcondition-delete.md)|Ninguno|Elimina un [circularGeofenceManagementCondition](../resources/intune-fencing-circulargeofencemanagementcondition.md).|
|[Actualizar circularGeofenceManagementCondition](../api/intune-fencing-circulargeofencemanagementcondition-update.md)|[circularGeofenceManagementCondition](../resources/intune-fencing-circulargeofencemanagementcondition.md)|Actualizar las propiedades de un objeto [circularGeofenceManagementCondition](../resources/intune-fencing-circulargeofencemanagementcondition.md) .|

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
|latitude|Doble|Latitud en grados, entre -90 y + 90 inclusive.|
|longitude|Doble|Longitud en grados, entre -180 y + 180 inclusive.|
|radiusInMeters|Single|Radio en metros.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|managementConditionStatements|colección de [managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md)|Las instrucciones de condición de administración asociadas a la condición de administración. Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.circularGeofenceManagementCondition"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.circularGeofenceManagementCondition",
  "id": "String (identifier)",
  "uniqueName": "String",
  "displayName": "String",
  "description": "String",
  "createdDateTime": "String (timestamp)",
  "modifiedDateTime": "String (timestamp)",
  "eTag": "String",
  "applicablePlatforms": [
    "String"
  ],
  "latitude": "<Unknown Primitive Type Edm.Double>",
  "longitude": "<Unknown Primitive Type Edm.Double>",
  "radiusInMeters": "<Unknown Primitive Type Edm.Single>"
}
```





