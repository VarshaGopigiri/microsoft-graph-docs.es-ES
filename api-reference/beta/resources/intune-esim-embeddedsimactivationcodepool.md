---
title: tipo de recurso embeddedSIMActivationCodePool
description: Un grupo representa un grupo de códigos de activación de SIM incrustados.
author: tfitzmac
ms.openlocfilehash: 9f756488d4e00e3d69bebf0e484f01aeec5650a7
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27307143"
---
# <a name="embeddedsimactivationcodepool-resource-type"></a>tipo de recurso embeddedSIMActivationCodePool

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Un grupo representa un grupo de códigos de activación de SIM incrustados.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista embeddedSIMActivationCodePools](../api/intune-esim-embeddedsimactivationcodepool-list.md)|colección de [embeddedSIMActivationCodePool](../resources/intune-esim-embeddedsimactivationcodepool.md)|Propiedades de la lista y relaciones de los objetos [embeddedSIMActivationCodePool](../resources/intune-esim-embeddedsimactivationcodepool.md) .|
|[Obtener embeddedSIMActivationCodePool](../api/intune-esim-embeddedsimactivationcodepool-get.md)|[embeddedSIMActivationCodePool](../resources/intune-esim-embeddedsimactivationcodepool.md)|Leer las propiedades y las relaciones del objeto [embeddedSIMActivationCodePool](../resources/intune-esim-embeddedsimactivationcodepool.md) .|
|[Crear embeddedSIMActivationCodePool](../api/intune-esim-embeddedsimactivationcodepool-create.md)|[embeddedSIMActivationCodePool](../resources/intune-esim-embeddedsimactivationcodepool.md)|Crear un nuevo objeto [embeddedSIMActivationCodePool](../resources/intune-esim-embeddedsimactivationcodepool.md) .|
|[Eliminar embeddedSIMActivationCodePool](../api/intune-esim-embeddedsimactivationcodepool-delete.md)|Ninguno|Elimina un [embeddedSIMActivationCodePool](../resources/intune-esim-embeddedsimactivationcodepool.md).|
|[Actualizar embeddedSIMActivationCodePool](../api/intune-esim-embeddedsimactivationcodepool-update.md)|[embeddedSIMActivationCodePool](../resources/intune-esim-embeddedsimactivationcodepool.md)|Actualizar las propiedades de un objeto [embeddedSIMActivationCodePool](../resources/intune-esim-embeddedsimactivationcodepool.md) .|
|[Acción assign](../api/intune-esim-embeddedsimactivationcodepool-assign.md)|colección de [embeddedSIMActivationCodePoolAssignment](../resources/intune-esim-embeddedsimactivationcodepoolassignment.md)|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Identificador único para el grupo de código de activación de SIM incrustado. Valor asignado al crear generada por el sistema.|
|displayName|String|El administrador definida por el nombre del grupo de código de activación SIM incrustado.|
|createdDateTime|DateTimeOffset|La hora en que se creó el grupo de código de activación de SIM incrustado. Servicio generado al lado.|
|modifiedDateTime|DateTimeOffset|La hora en que se modificó por última vez el grupo de código de activación de SIM incrustado. Se actualizó el lado de servicio.|
|activationCodes|colección de [embeddedSIMActivationCode](../resources/intune-esim-embeddedsimactivationcode.md)|Los códigos de activación que pertenecen a este grupo de servidores. Esta propiedad de navegación se usa para registrar los códigos de activación para Intune pero no se puede usar para leer los códigos de activación de Intune.|
|activationCodeCount|Int32|El número total de códigos de activación que pertenecen a este grupo de servidores.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|asignaciones|colección de [embeddedSIMActivationCodePoolAssignment](../resources/intune-esim-embeddedsimactivationcodepoolassignment.md)|Propiedad de navegación a una lista de destinos al que está asignado este grupo de servidores.|
|deviceStates|colección de [embeddedSIMDeviceState](../resources/intune-esim-embeddedsimdevicestate.md)|Propiedad de navegación a una lista de Estados de dispositivo para este grupo de servidores.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.embeddedSIMActivationCodePool"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.embeddedSIMActivationCodePool",
  "id": "String (identifier)",
  "displayName": "String",
  "createdDateTime": "String (timestamp)",
  "modifiedDateTime": "String (timestamp)",
  "activationCodes": [
    {
      "@odata.type": "microsoft.graph.embeddedSIMActivationCode",
      "integratedCircuitCardIdentifier": "String",
      "matchingIdentifier": "String",
      "smdpPlusServerAddress": "String"
    }
  ],
  "activationCodeCount": 1024
}
```





