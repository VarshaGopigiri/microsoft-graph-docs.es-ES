---
title: Tipo de recurso deviceComplianceActionItem
description: Configuración de la acción programada
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 46828e3379fbf5179658ed7e2fb2e5e960d61ada
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27965708"
---
# <a name="devicecomplianceactionitem-resource-type"></a>Tipo de recurso deviceComplianceActionItem

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Configuración de la acción programada
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar deviceComplianceActionItems](../api/intune-deviceconfig-devicecomplianceactionitem-list.md)|Colección [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md)|Enumere las propiedades y las relaciones de los objetos [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md).|
|[Obtener deviceComplianceActionItem](../api/intune-deviceconfig-devicecomplianceactionitem-get.md)|[deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md)|Lea las propiedades y las relaciones de los objetos [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md).|
|[Crear deviceComplianceActionItem](../api/intune-deviceconfig-devicecomplianceactionitem-create.md)|[deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md)|Cree un objeto [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md).|
|[Eliminar deviceComplianceActionItem](../api/intune-deviceconfig-devicecomplianceactionitem-delete.md)|Ninguna|Elimina un [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md).|
|[Actualizar deviceComplianceActionItem](../api/intune-deviceconfig-devicecomplianceactionitem-update.md)|[deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md)|Actualice las propiedades de un objeto [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad.|
|gracePeriodHours|Int32|Número de horas de espera hasta que se aplica la acción. Valores válidos de 0 a 8760|
|actionType|[deviceComplianceActionType](../resources/intune-deviceconfig-devicecomplianceactiontype.md)|¿Qué acción debe realizar. Los valores posibles son: `noAction`, `notification`, `block`, `retire`, `wipe`, `removeResourceAccessProfiles` y `pushNotification`.|
|notificationTemplateId|String|Qué plantilla de mensaje de notificación usar|
|notificationMessageCCList|Colección string|Una lista de identificadores de grupo para especificar a quién enviar este mensaje de notificación.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceComplianceActionItem"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceComplianceActionItem",
  "id": "String (identifier)",
  "gracePeriodHours": 1024,
  "actionType": "String",
  "notificationTemplateId": "String",
  "notificationMessageCCList": [
    "String"
  ]
}
```



