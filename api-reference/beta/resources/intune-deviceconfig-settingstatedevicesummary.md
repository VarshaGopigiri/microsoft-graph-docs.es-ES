---
title: Tipo de recurso settingStateDeviceSummary
description: Directiva de cumplimiento y configuración del dispositivo para ver un resumen de estado de la configuración
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 2104998cfdd65659114b1850d3cfcf1392bf9642
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27925878"
---
# <a name="settingstatedevicesummary-resource-type"></a>Tipo de recurso settingStateDeviceSummary

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Directiva de cumplimiento y configuración del dispositivo para ver un resumen de estado de la configuración
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar settingStateDeviceSummaries](../api/intune-deviceconfig-settingstatedevicesummary-list.md)|Colección [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md)|Enumere las propiedades y las relaciones de los objetos [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md).|
|[Obtener settingStateDeviceSummary](../api/intune-deviceconfig-settingstatedevicesummary-get.md)|[settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md)|Lea las propiedades y las relaciones del objeto [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md).|
|[Crear settingStateDeviceSummary](../api/intune-deviceconfig-settingstatedevicesummary-create.md)|[settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md)|Cree un objeto [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md).|
|[Eliminar settingStateDeviceSummary](../api/intune-deviceconfig-settingstatedevicesummary-delete.md)|Ninguna|Elimina un [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md).|
|[Actualizar settingStateDeviceSummary](../api/intune-deviceconfig-settingstatedevicesummary-update.md)|[settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md)|Actualice las propiedades de un objeto [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad.|
|settingName|String|Nombre de la configuración|
|instancePath|String|Nombre de InstancePath para la configuración|
|unknownDeviceCount|Int32|Número de dispositivos desconocido para la configuración|
|notApplicableDeviceCount|Int32|Número de dispositivos no aplicables para la configuración|
|compliantDeviceCount|Int32|Número de dispositivos compatibles para la configuración|
|remediatedDeviceCount|Int32|Número de dispositivos compatibles para la configuración|
|nonCompliantDeviceCount|Int32|Número de dispositivos no compatibles para la configuración|
|errorDeviceCount|Int32|Número de errores de dispositivo para la configuración|
|conflictDeviceCount|Int32|Número de errores de conflictos de dispositivo para la configuración|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.settingStateDeviceSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.settingStateDeviceSummary",
  "id": "String (identifier)",
  "settingName": "String",
  "instancePath": "String",
  "unknownDeviceCount": 1024,
  "notApplicableDeviceCount": 1024,
  "compliantDeviceCount": 1024,
  "remediatedDeviceCount": 1024,
  "nonCompliantDeviceCount": 1024,
  "errorDeviceCount": 1024,
  "conflictDeviceCount": 1024
}
```





