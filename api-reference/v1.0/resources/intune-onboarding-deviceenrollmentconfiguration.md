---
title: Tipo de recurso deviceEnrollmentConfiguration
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: 6d3c8b1114a19429f89d5f5b6b466a1dec12eb26
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27326582"
---
# <a name="deviceenrollmentconfiguration-resource-type"></a>Tipo de recurso deviceEnrollmentConfiguration

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar deviceEnrollmentConfigurations](../api/intune-onboarding-deviceenrollmentconfiguration-list.md)|Colección [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)|Enumere las propiedades y las relaciones de los objetos [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md).|
|[Obtener deviceEnrollmentConfiguration](../api/intune-onboarding-deviceenrollmentconfiguration-get.md)|[deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)|Lea las propiedades y las relaciones del objeto [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md).|
|[Acción setPriority](../api/intune-onboarding-deviceenrollmentconfiguration-setpriority.md)|Ninguna|Todavía no documentado|
|[Acción assign](../api/intune-onboarding-deviceenrollmentconfiguration-assign.md)|Ninguno|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Todavía no documentado|
|displayName|String|Todavía no documentado|
|descripción|String|Todavía no documentado|
|prioridad|Int32|Todavía no documentado|
|createdDateTime|DateTimeOffset|Todavía no documentado|
|lastModifiedDateTime|DateTimeOffset|Todavía no documentado|
|versión|Int32|Todavía no documentado|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|Asignaciones|Colección [enrollmentConfigurationAssignment](../resources/intune-onboarding-enrollmentconfigurationassignment.md)|La lista de asignaciones de grupo para el perfil de configuración del dispositivo.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceEnrollmentConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceEnrollmentConfiguration",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "priority": 1024,
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "version": 1024
}
```



