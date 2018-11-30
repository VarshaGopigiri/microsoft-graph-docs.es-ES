---
title: Tipo de recurso reportRoot
description: El recurso que representa una instancia del historial de informes.
ms.openlocfilehash: 6f944351c0099270d1d16ca15a9ae1f41629174b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029854"
---
# <a name="reportroot-resource-type"></a>Tipo de recurso reportRoot

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El recurso que representa una instancia del historial de informes.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener reportRoot](../api/intune-shared-reportroot-get.md)|[reportRoot](../resources/intune-shared-reportroot.md)|Lea las propiedades y las relaciones del objeto [reportRoot](../resources/intune-shared-reportroot.md).|
|[Actualizar reportRoot](../api/intune-shared-reportroot-update.md)|[reportRoot](../resources/intune-shared-reportroot.md)|Actualice las propiedades de un objeto [reportRoot](../resources/intune-shared-reportroot.md).|
|**Configuración de dispositivos**|
|[Función deviceConfigurationDeviceActivity](../api/intune-shared-reportroot-deviceconfigurationdeviceactivity.md)|[report](../resources/intune-shared-report.md)|Metadatos para el informe de actividad de dispositivo de configuración de dispositivo|
|[Función deviceConfigurationUserActivity](../api/intune-shared-reportroot-deviceconfigurationuseractivity.md)|[report](../resources/intune-shared-report.md)|Metadatos para el informe de actividad de usuario de configuración de dispositivo|
|**Solución de problemas**|
|[managedDeviceEnrollmentFailureDetails (función)](../api/intune-shared-reportroot-manageddeviceenrollmentfailuredetails.md)|[report](../resources/intune-shared-report.md)|Todavía no está documentada.|
|[managedDeviceEnrollmentTopFailures (función)](../api/intune-shared-reportroot-manageddeviceenrollmenttopfailures.md)|[report](../resources/intune-shared-report.md)|Todavía no está documentada.|


## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|El identificador único de esta entidad.|

## <a name="relationships"></a>Relaciones
Ninguna

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.reportRoot"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.reportRoot",
  "id": "String (identifier)"
}
```

## <a name="example"></a>Ejemplo

<!--{"blockType": "request"}-->
```http
GET https://graph.microsoft.com/v1.0/reports
```

<!--{"blockType": "response", "truncated": true, "@odata.type": "microsoft.graph.reportRoot"}-->
```json
HTTP/1.1 200 OK
Content-Type: application/json

{
}
```