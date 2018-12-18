---
title: Tipo de recurso deviceEnrollmentPlatformRestrictionsConfiguration
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: 7463dbbfd28bc1b2138c862dc909933a683e7fac
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27343550"
---
# <a name="deviceenrollmentplatformrestrictionsconfiguration-resource-type"></a>Tipo de recurso deviceEnrollmentPlatformRestrictionsConfiguration

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado

Hereda de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar deviceEnrollmentPlatformRestrictionsConfigurations](../api/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration-list.md)|Colección [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md)|Enumere las propiedades y las relaciones de los objetos [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md).|
|[Obtener deviceEnrollmentPlatformRestrictionsConfiguration](../api/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration-get.md)|[deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md)|Lea las propiedades y las relaciones del objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md).|
|[Crear deviceEnrollmentPlatformRestrictionsConfiguration](../api/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration-create.md)|[deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md)|Cree un objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md).|
|[Eliminar deviceEnrollmentPlatformRestrictionsConfiguration](../api/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration-delete.md)|Ninguna|Elimina un [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md).|
|[Actualizar deviceEnrollmentPlatformRestrictionsConfiguration](../api/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration-update.md)|[deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md)|Actualice las propiedades de un objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune-onboarding-deviceenrollmentplatformrestrictionsconfiguration.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)|
|displayName|String|Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)|
|descripción|String|Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)|
|prioridad|Int32|Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)|
|createdDateTime|DateTimeOffset|Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)|
|lastModifiedDateTime|DateTimeOffset|Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)|
|version|Int32|Todavía no documentado Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)|
|iosRestriction|[deviceEnrollmentPlatformRestriction](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|Todavía no documentado|
|windowsRestriction|[deviceEnrollmentPlatformRestriction](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|Todavía no documentado|
|windowsMobileRestriction|[deviceEnrollmentPlatformRestriction](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|Todavía no documentado|
|androidRestriction|[deviceEnrollmentPlatformRestriction](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|Todavía no documentado|
|macOSRestriction|[deviceEnrollmentPlatformRestriction](../resources/intune-onboarding-deviceenrollmentplatformrestriction.md)|Todavía no documentado|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|Asignaciones|Colección [enrollmentConfigurationAssignment](../resources/intune-onboarding-enrollmentconfigurationassignment.md)|La lista de asignaciones de grupo para el perfil de configuración del dispositivo. Heredado de [deviceEnrollmentConfiguration](../resources/intune-onboarding-deviceenrollmentconfiguration.md)|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestrictionsConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceEnrollmentPlatformRestrictionsConfiguration",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "priority": 1024,
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "version": 1024,
  "iosRestriction": {
    "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
    "platformBlocked": true,
    "personalDeviceEnrollmentBlocked": true,
    "osMinimumVersion": "String",
    "osMaximumVersion": "String"
  },
  "windowsRestriction": {
    "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
    "platformBlocked": true,
    "personalDeviceEnrollmentBlocked": true,
    "osMinimumVersion": "String",
    "osMaximumVersion": "String"
  },
  "windowsMobileRestriction": {
    "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
    "platformBlocked": true,
    "personalDeviceEnrollmentBlocked": true,
    "osMinimumVersion": "String",
    "osMaximumVersion": "String"
  },
  "androidRestriction": {
    "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
    "platformBlocked": true,
    "personalDeviceEnrollmentBlocked": true,
    "osMinimumVersion": "String",
    "osMaximumVersion": "String"
  },
  "macOSRestriction": {
    "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
    "platformBlocked": true,
    "personalDeviceEnrollmentBlocked": true,
    "osMinimumVersion": "String",
    "osMaximumVersion": "String"
  }
}
```



