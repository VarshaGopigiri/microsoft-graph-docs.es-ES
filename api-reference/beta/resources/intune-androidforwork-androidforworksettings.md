---
title: Tipo de recurso androidForWorkSettings
description: Configuración de Android for Work
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: c2bbcb9f21750d1f1f3a07a1567bbf2f8f822e53
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27933571"
---
# <a name="androidforworksettings-resource-type"></a>Tipo de recurso androidForWorkSettings

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Configuración de Android for Work
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener androidForWorkSettings](../api/intune-androidforwork-androidforworksettings-get.md)|[androidForWorkSettings](../resources/intune-androidforwork-androidforworksettings.md)|Lea las propiedades y las relaciones del objeto [androidForWorkSettings](../resources/intune-androidforwork-androidforworksettings.md).|
|[Actualizar androidForWorkSettings](../api/intune-androidforwork-androidforworksettings-update.md)|[androidForWorkSettings](../resources/intune-androidforwork-androidforworksettings.md)|Actualice las propiedades de un objeto [androidForWorkSettings](../resources/intune-androidforwork-androidforworksettings.md).|
|[Acción requestSignupUrl](../api/intune-androidforwork-androidforworksettings-requestsignupurl.md)|cadena|Todavía no documentado|
|[Acción completeSignup](../api/intune-androidforwork-androidforworksettings-completesignup.md)|Ninguna|Todavía no documentado|
|[Acción syncApps](../api/intune-androidforwork-androidforworksettings-syncapps.md)|Ninguna|Todavía no documentado|
|[Acción unbind](../api/intune-androidforwork-androidforworksettings-unbind.md)|Ninguna|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Identificador de la configuración de Android for Work|
|bindStatus|[androidForWorkBindStatus](../resources/intune-androidforwork-androidforworkbindstatus.md)|Enlazar el estado del inquilino con la API de Google EMM. Los valores posibles son: `notBound`, `bound`, `boundAndValidated` y `unbinding`.|
|lastAppSyncDateTime|DateTimeOffset|Última hora de finalización para la sincronización de la aplicación|
|lastAppSyncStatus|[androidForWorkSyncStatus](../resources/intune-androidforwork-androidforworksyncstatus.md)|Resultado de la última sincronización de aplicación. Los valores posibles son: `success`, `credentialsNotValid`, `androidForWorkApiError`, `managementServiceError`, `unknownError`, `none`.|
|ownerUserPrincipalName|String|UPN del propietario que creó la empresa|
|ownerOrganizationName|String|Nombre de organización usado al incorporar Android for Work|
|lastModifiedDateTime|DateTimeOffset|Última hora de modificación para la configuración de Android for Work|
|enrollmentTarget|[androidForWorkEnrollmentTarget](../resources/intune-androidforwork-androidforworkenrollmenttarget.md)|Indica qué usuarios pueden inscribirse dispositivos para Android para administración de dispositivos de trabajo. Los valores posibles son: `none`, `all`, `targeted` y `targetedAsEnrollmentRestrictions`.|
|targetGroupIds|Colección String|Especifica los grupos de AAD que pueden inscribir dispositivos en la administración de dispositivos de Android for Work si se establece enrollmentTarget en "Dirigido"|
|deviceOwnerManagementEnabled|Booleano|Indica si esta cuenta es flighting para la administración de propietario dispositivos Android con CloudDPC.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.androidForWorkSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.androidForWorkSettings",
  "id": "String (identifier)",
  "bindStatus": "String",
  "lastAppSyncDateTime": "String (timestamp)",
  "lastAppSyncStatus": "String",
  "ownerUserPrincipalName": "String",
  "ownerOrganizationName": "String",
  "lastModifiedDateTime": "String (timestamp)",
  "enrollmentTarget": "String",
  "targetGroupIds": [
    "String"
  ],
  "deviceOwnerManagementEnabled": true
}
```





