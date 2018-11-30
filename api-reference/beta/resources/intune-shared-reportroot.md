---
title: Tipo de recurso reportRoot
description: El recurso que representa una instancia de un dispositivo o del informe para solucionar problemas, según el contexto.
ms.openlocfilehash: 581f13bd7383be31ccdce7e536626eb6375ba777
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083459"
---
# <a name="reportroot-resource-type"></a>Tipo de recurso reportRoot

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El recurso que representa una instancia de un dispositivo o del informe para solucionar problemas, según el contexto.

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener reportRoot](../api/intune-shared-reportroot-get.md)|Lea las propiedades y las relaciones del objeto [reportRoot](../resources/intune-shared-reportroot.md).|
|[Actualizar reportRoot](../api/intune-shared-reportroot-update.md)|Actualice las propiedades de un objeto [reportRoot](../resources/intune-shared-reportroot.md).|
|**Configuración de dispositivos**|
|[Función deviceConfigurationUserActivity](../api/intune-shared-reportroot-deviceconfigurationuseractivity.md)|Metadatos para el informe de actividad de usuario de configuración de dispositivo|
|[Función deviceConfigurationDeviceActivity](../api/intune-shared-reportroot-deviceconfigurationdeviceactivity.md)|Metadatos para el informe de actividad de dispositivo de configuración de dispositivo|
|**Solución de problemas**|
|[managedDeviceEnrollmentAbandonmentDetails (función)](../api/intune-shared-reportroot-manageddeviceenrollmentabandonmentdetails.md)|[report](../resources/intune-shared-report.md)|Informe detallan de metadatos por abandono de inscripción|
|[managedDeviceEnrollmentAbandonmentSummary (función)](../api/intune-shared-reportroot-manageddeviceenrollmentabandonmentsummary.md)|[report](../resources/intune-shared-report.md)|Metadatos para el informe de resumen de abandono de inscripción|
|[managedDeviceEnrollmentFailureDetails (función)](../api/intune-shared-reportroot-manageddeviceenrollmentfailuredetails.md)|Todavía no documentado|
|[managedDeviceEnrollmentFailureTrends (función)](../api/intune-shared-reportroot-manageddeviceenrollmentfailuretrends.md)|Metadatos para el informe de tendencias de errores de inscripción|
|[managedDeviceEnrollmentTopFailures (función)](../api/intune-shared-reportroot-manageddeviceenrollmenttopfailures.md)|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|El identificador único de esta entidad.|

## <a name="relationships"></a>Relaciones
Ninguna

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.reportRoot"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.reportRoot",
  "id": "String (identifier)"
}
```



