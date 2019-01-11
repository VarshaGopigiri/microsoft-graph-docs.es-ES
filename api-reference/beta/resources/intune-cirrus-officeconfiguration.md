---
title: tipo de recurso officeConfiguration
description: Entidad singleton que actúa como un contenedor para todas las funcionalidades de administración de dispositivos.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 096a54db296181e58020bb9bc694056c0b9e949a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27817264"
---
# <a name="officeconfiguration-resource-type"></a>tipo de recurso officeConfiguration

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Entidad singleton que actúa como un contenedor para todas las funcionalidades de administración de dispositivos.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|Obtener officeConfiguration|[officeConfiguration](../resources/intune-cirrus-officeconfiguration.md)|Leer las propiedades y las relaciones del objeto [officeConfiguration](../resources/intune-cirrus-officeconfiguration.md) .|
|Actualizar officeConfiguration|[officeConfiguration](../resources/intune-cirrus-officeconfiguration.md)|Actualizar las propiedades de un objeto [officeConfiguration](../resources/intune-cirrus-officeconfiguration.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Identificador de la configuración de office.|
|tenantCheckinStatuses|colección de [officeClientCheckinStatus](../resources/intune-cirrus-officeclientcheckinstatus.md)|Lista de comprobación de estado del cliente de office.|
|tenantUserCheckinSummary|[officeUserCheckinSummary](../resources/intune-cirrus-officeusercheckinsummary.md)|Entidad que describe el inquilino de verificación estatuas|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Description|
|:---|:---|:---|
|clientConfigurations|colección de [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)|Lista de configuración de cliente de office.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.officeConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.officeConfiguration",
  "id": "String (identifier)",
  "tenantCheckinStatuses": [
    {
      "@odata.type": "microsoft.graph.officeClientCheckinStatus",
      "userPrincipalName": "String",
      "deviceName": "String",
      "devicePlatform": "String",
      "devicePlatformVersion": "String",
      "wasSuccessful": true,
      "userId": "String",
      "checkinDateTime": "String (timestamp)",
      "errorMessage": "String",
      "appliedPolicies": [
        "String"
      ]
    }
  ],
  "tenantUserCheckinSummary": {
    "@odata.type": "microsoft.graph.officeUserCheckinSummary",
    "succeededUserCount": 1024,
    "failedUserCount": 1024
  }
}
```



