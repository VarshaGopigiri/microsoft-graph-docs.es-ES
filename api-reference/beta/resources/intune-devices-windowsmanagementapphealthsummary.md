---
title: tipo de recurso windowsManagementAppHealthSummary
description: Contiene las propiedades para el resumen de estado de la aplicación de administración de Windows.
ms.openlocfilehash: dddcb40a0a66446ab6e87a2e684c1dbf0df547fc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086780"
---
# <a name="windowsmanagementapphealthsummary-resource-type"></a>tipo de recurso windowsManagementAppHealthSummary

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades para el resumen de estado de la aplicación de administración de Windows.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener windowsManagementAppHealthSummary](../api/intune-devices-windowsmanagementapphealthsummary-get.md)|[windowsManagementAppHealthSummary](../resources/intune-devices-windowsmanagementapphealthsummary.md)|Leer las propiedades y las relaciones del objeto [windowsManagementAppHealthSummary](../resources/intune-devices-windowsmanagementapphealthsummary.md) .|
|[Actualizar windowsManagementAppHealthSummary](../api/intune-devices-windowsmanagementapphealthsummary-update.md)|[windowsManagementAppHealthSummary](../resources/intune-devices-windowsmanagementapphealthsummary.md)|Actualizar las propiedades de un objeto [windowsManagementAppHealthSummary](../resources/intune-devices-windowsmanagementapphealthsummary.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad resumen del estado de aplicación de Windows management.|
|healthyDeviceCount|Int32|Recuento de dispositivo correcto.|
|unhealthyDeviceCount|Int32|Recuento de dispositivo mal estado.|
|unknownDeviceCount|Int32|Recuento de dispositivo desconocido.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsManagementAppHealthSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsManagementAppHealthSummary",
  "id": "String (identifier)",
  "healthyDeviceCount": 1024,
  "unhealthyDeviceCount": 1024,
  "unknownDeviceCount": 1024
}
```





