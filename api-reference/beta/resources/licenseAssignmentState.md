---
title: tipo de recurso licenseAssignmentState
description: 'La propiedad **licenseAssignmentStates** de la entidad de usuario es una colección de **licenseAssignmentState**. Proporciona información detallada acerca de las asignaciones de licencia a un usuario. Los detalles se incluye información como:  '
ms.openlocfilehash: 4e7101acc756a845913a081368b79242834ef3bd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088895"
---
# <a name="licenseassignmentstate-resource-type"></a>tipo de recurso licenseAssignmentState

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

La propiedad **licenseAssignmentStates** de la entidad de [usuario](user.md) es una colección de **licenseAssignmentState**. Proporciona información detallada acerca de las asignaciones de licencia a un usuario. Los detalles se incluye información como:  

 - ¿Qué planes están deshabilitados para un usuario
 - Si la licencia se ha asignado al usuario directamente o se hereda de un grupo de
 - Estado actual de la asignación
 - Si el estado de la asignación es Error, ¿cuál es el detalle de error para el error? 


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|assignedByGroup|string|El identificador del grupo al que se asigna esta licencia. Si la asignación es una licencia asignada directos, este campo será Null. Solo lectura.|
|disabledPlans|Collection(String)|Los planes de servicio que están deshabilitados en esta asignación. Solo lectura.|
|error|String|Error de asignación de licencia. Si la licencia está asignada correctamente, este campo será Null. Solo lectura. Valores posibles: `CountViolation`, `MutuallyExclusiveViolation`, `DependencyViolation`, `ProhibitedInUsageLocationViolation`, `UniquenessViolation`, y `Others`. Para obtener más información acerca de cómo identificar y resolver la asignación de licencias de errores, consulte [aquí](https://docs.microsoft.com/azure/active-directory/users-groups-roles/licensing-groups-resolve-problems).|
|skuId|String|Identificador único de la SKU. Solo lectura.|
|estado|String|Indicar el estado actual de esta asignación. Solo lectura. Valores posibles: activo, ActiveWithError, deshabilitado y Error.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

```json
{
  "assignedByGroup": "String",
  "disabledPlans": "Collection(String)",
  "error": " String ",  
  "skuId": "String ",
  "state": "String"
}

```