---
title: Tipo de recurso deviceComplianceScheduledActionForRule
description: Acción programada para la regla
author: tfitzmac
ms.openlocfilehash: 912a0722b85857aa64daa5339cc7730a4c0413ed
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27344775"
---
# <a name="devicecompliancescheduledactionforrule-resource-type"></a>Tipo de recurso deviceComplianceScheduledActionForRule

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Acción programada para la regla
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar deviceComplianceScheduledActionForRules](../api/intune-deviceconfig-devicecompliancescheduledactionforrule-list.md)|Colección [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md)|Enumere las propiedades y las relaciones de los objetos [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md).|
|[Obtener deviceComplianceScheduledActionForRule](../api/intune-deviceconfig-devicecompliancescheduledactionforrule-get.md)|[deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md)|Lea las propiedades y las relaciones del objeto [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md).|
|[Crear deviceComplianceScheduledActionForRule](../api/intune-deviceconfig-devicecompliancescheduledactionforrule-create.md)|[deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md)|Cree un objeto [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md).|
|[Eliminar deviceComplianceScheduledActionForRule](../api/intune-deviceconfig-devicecompliancescheduledactionforrule-delete.md)|Ninguna|Elimina un [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md).|
|[Actualizar deviceComplianceScheduledActionForRule](../api/intune-deviceconfig-devicecompliancescheduledactionforrule-update.md)|[deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md)|Actualice las propiedades de un objeto [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad.|
|ruleName|String|Nombre de la regla a la que se aplica esta acción programada.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|scheduledActionConfigurations|Colección [deviceComplianceActionItem](../resources/intune-deviceconfig-devicecomplianceactionitem.md)|La lista de las configuraciones de las acciones programadas para esta directiva de cumplimiento.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceComplianceScheduledActionForRule"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceComplianceScheduledActionForRule",
  "id": "String (identifier)",
  "ruleName": "String"
}
```





