---
title: tipo de recurso embeddedSIMActivationCodePoolAssignment
description: La entidad de asignación grupo incrustada del código de activación SIM asigna un embeddedSIMActivationCodePool específico a un grupo de dispositivos AAD.
author: tfitzmac
ms.openlocfilehash: 67d563a630fb1c1092416f1081c4decda0d9eaf4
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27337439"
---
# <a name="embeddedsimactivationcodepoolassignment-resource-type"></a>tipo de recurso embeddedSIMActivationCodePoolAssignment

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

La entidad de asignación grupo incrustada del código de activación SIM asigna un embeddedSIMActivationCodePool específico a un grupo de dispositivos AAD.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista embeddedSIMActivationCodePoolAssignments](../api/intune-esim-embeddedsimactivationcodepoolassignment-list.md)|colección de [embeddedSIMActivationCodePoolAssignment](../resources/intune-esim-embeddedsimactivationcodepoolassignment.md)|Propiedades de la lista y relaciones de los objetos [embeddedSIMActivationCodePoolAssignment](../resources/intune-esim-embeddedsimactivationcodepoolassignment.md) .|
|[Obtener embeddedSIMActivationCodePoolAssignment](../api/intune-esim-embeddedsimactivationcodepoolassignment-get.md)|[embeddedSIMActivationCodePoolAssignment](../resources/intune-esim-embeddedsimactivationcodepoolassignment.md)|Leer las propiedades y las relaciones del objeto [embeddedSIMActivationCodePoolAssignment](../resources/intune-esim-embeddedsimactivationcodepoolassignment.md) .|
|[Crear embeddedSIMActivationCodePoolAssignment](../api/intune-esim-embeddedsimactivationcodepoolassignment-create.md)|[embeddedSIMActivationCodePoolAssignment](../resources/intune-esim-embeddedsimactivationcodepoolassignment.md)|Crear un nuevo objeto [embeddedSIMActivationCodePoolAssignment](../resources/intune-esim-embeddedsimactivationcodepoolassignment.md) .|
|[Eliminar embeddedSIMActivationCodePoolAssignment](../api/intune-esim-embeddedsimactivationcodepoolassignment-delete.md)|Ninguno|Elimina un [embeddedSIMActivationCodePoolAssignment](../resources/intune-esim-embeddedsimactivationcodepoolassignment.md).|
|[Actualizar embeddedSIMActivationCodePoolAssignment](../api/intune-esim-embeddedsimactivationcodepoolassignment-update.md)|[embeddedSIMActivationCodePoolAssignment](../resources/intune-esim-embeddedsimactivationcodepoolassignment.md)|Actualizar las propiedades de un objeto [embeddedSIMActivationCodePoolAssignment](../resources/intune-esim-embeddedsimactivationcodepoolassignment.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Identificador único para la asignación de grupo de código de activación SIM incrustada. Valor asignado al crear generada por el sistema.|
|target|[deviceAndAppManagementAssignmentTarget](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|El tipo de grupos de destino mediante el grupo de código de activación de SIM incrustado.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.embeddedSIMActivationCodePoolAssignment"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.embeddedSIMActivationCodePoolAssignment",
  "id": "String (identifier)",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```





