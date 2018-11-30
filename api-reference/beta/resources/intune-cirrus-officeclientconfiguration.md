---
title: tipo de recurso officeClientConfiguration
description: Configuración de cliente de Office.
ms.openlocfilehash: de510d7a57c10d1f74a3e58856afb9233243ec17
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086109"
---
# <a name="officeclientconfiguration-resource-type"></a>tipo de recurso officeClientConfiguration

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Configuración de cliente de Office.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista officeClientConfigurations](../api/intune-cirrus-officeclientconfiguration-list.md)|colección de [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)|Propiedades de la lista y relaciones de los objetos [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md) .|
|[Obtener officeClientConfiguration](../api/intune-cirrus-officeclientconfiguration-get.md)|[officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)|Leer las propiedades y las relaciones del objeto [officeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md) .|
|[Acción assign](../api/intune-cirrus-officeclientconfiguration-assign.md)|colección de [officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md)|Reemplazar todos los grupos para una directiva.|
|[acción updatePriorities](../api/intune-cirrus-officeclientconfiguration-updatepriorities.md)|Ninguno|Actualizar las prioridades de directiva.|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Identificador de la directiva de configuración de cliente de office.|
|userPreferencePayload|Stream|Configuración de preferencias de JSON de cadenas en formato binario, estos valores pueden ser anulados por el usuario.|
|policyPayload|Stream|Configuración de la directiva JSON de cadenas en formato binario, no se puede cambiar estos valores por el usuario.|
|descripción|String|Todavía no documentado|
|displayName|String|Administración descripción proporcionada por el del cliente de office de directiva de configuración.|
|lastModifiedDateTime|DateTime|Última marca de datetime modificada de la directiva.|
|prioridad|Int32|Valor de prioridad debe ser un valor único para cada directiva de un inquilino y se usará para la resolución de conflictos, los valores más bajos significan prioridad sea alta.|
|userCheckinSummary|[officeUserCheckinSummary](../resources/intune-cirrus-officeusercheckinsummary.md)|Protección de resumen de usuario para la directiva.|
|checkinStatuses|colección de [officeClientCheckinStatus](../resources/intune-cirrus-officeclientcheckinstatus.md)|Lista de comprobación de estado del cliente de office.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|asignaciones|colección de [officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md)|La lista de las asignaciones de grupo para la directiva.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.officeClientConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.officeClientConfiguration",
  "id": "String (identifier)",
  "userPreferencePayload": "<Unknown Primitive Type Edm.Stream>",
  "policyPayload": "<Unknown Primitive Type Edm.Stream>",
  "description": "String",
  "displayName": "String",
  "priority": 1024,
  "userCheckinSummary": {
    "@odata.type": "microsoft.graph.officeUserCheckinSummary",
    "succeededUserCount": 1024,
    "failedUserCount": 1024
  },
  "checkinStatuses": [
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
  ]
}
```



