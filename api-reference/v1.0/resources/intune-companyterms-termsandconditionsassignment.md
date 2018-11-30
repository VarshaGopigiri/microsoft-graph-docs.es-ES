---
title: Tipo de recurso termsAndConditionsAssignment
description: C) de la directiva a un grupo determinado. Se solicitará a los usuarios del grupo que acepten los términos para inscribir sus dispositivos en Intune.
ms.openlocfilehash: 848998e59f214fc679aba7c27a2a529be05c8adc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031375"
---
# <a name="termsandconditionsassignment-resource-type"></a>Tipo de recurso termsAndConditionsAssignment

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Una entidad termsAndConditionsAssignment representa la asignación de una directiva de Términos y condiciones (TyC) determinada para un grupo específico. Se solicitará a los usuarios del grupo que acepten los términos para inscribir sus dispositivos en Intune.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar termsAndConditionsAssignments](../api/intune-companyterms-termsandconditionsassignment-list.md)|Colección [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md)|Enumere las propiedades y las relaciones de los objetos [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md).|
|[Obtener termsAndConditionsAssignment](../api/intune-companyterms-termsandconditionsassignment-get.md)|[termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md)|Lea las propiedades y las relaciones del objeto [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md).|
|[Crear termsAndConditionsAssignment](../api/intune-companyterms-termsandconditionsassignment-create.md)|[termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md)|Cree un objeto [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md).|
|[Eliminar termsAndConditionsAssignment](../api/intune-companyterms-termsandconditionsassignment-delete.md)|Ninguna|Elimina un [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md)|
|[Actualizar termsAndConditionsAssignment](../api/intune-companyterms-termsandconditionsassignment-update.md)|[termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md)|Actualice las propiedades de un objeto [termsAndConditionsAssignment](../resources/intune-companyterms-termsandconditionsassignment.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Identificador único de la entidad.|
|target|[deviceAndAppManagementAssignmentTarget](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|Destino de asignación al que está asignada la directiva de términos y condiciones.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.termsAndConditionsAssignment"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.termsAndConditionsAssignment",
  "id": "String (identifier)",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```



