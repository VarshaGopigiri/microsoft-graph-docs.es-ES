---
title: tipo de recurso androidManagedStoreAccountEnterpriseSettings
description: Configuración de la empresa para un Android administrados cuenta de almacenamiento.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: db31210da358a8b6b7ebc674699dab4c622ae670
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27869037"
---
# <a name="androidmanagedstoreaccountenterprisesettings-resource-type"></a>tipo de recurso androidManagedStoreAccountEnterpriseSettings

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Configuración de la empresa para un Android administrados cuenta de almacenamiento.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener androidManagedStoreAccountEnterpriseSettings](../api/intune-androidforwork-androidmanagedstoreaccountenterprisesettings-get.md)|[androidManagedStoreAccountEnterpriseSettings](../resources/intune-androidforwork-androidmanagedstoreaccountenterprisesettings.md)|Leer las propiedades y las relaciones del objeto [androidManagedStoreAccountEnterpriseSettings](../resources/intune-androidforwork-androidmanagedstoreaccountenterprisesettings.md) .|
|[Actualizar androidManagedStoreAccountEnterpriseSettings](../api/intune-androidforwork-androidmanagedstoreaccountenterprisesettings-update.md)|[androidManagedStoreAccountEnterpriseSettings](../resources/intune-androidforwork-androidmanagedstoreaccountenterprisesettings.md)|Actualizar las propiedades de un objeto [androidManagedStoreAccountEnterpriseSettings](../resources/intune-androidforwork-androidmanagedstoreaccountenterprisesettings.md) .|
|[Acción requestSignupUrl](../api/intune-androidforwork-androidmanagedstoreaccountenterprisesettings-requestsignupurl.md)|cadena|Todavía no documentado|
|[Acción completeSignup](../api/intune-androidforwork-androidmanagedstoreaccountenterprisesettings-completesignup.md)|Ninguna|Todavía no documentado|
|[Acción syncApps](../api/intune-androidforwork-androidmanagedstoreaccountenterprisesettings-syncapps.md)|Ninguna|Todavía no documentado|
|[Acción unbind](../api/intune-androidforwork-androidmanagedstoreaccountenterprisesettings-unbind.md)|Ninguna|Todavía no documentado|
|[acción createGooglePlayWebToken](../api/intune-androidforwork-androidmanagedstoreaccountenterprisesettings-creategoogleplaywebtoken.md)|Cadena|Genera un token de web que se usa en un componente puede incrustar.|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|El Android almacenar el identificador de configuración de cuenta de empresa|
|bindStatus|[androidManagedStoreAccountBindStatus](../resources/intune-androidforwork-androidmanagedstoreaccountbindstatus.md)|Enlazar el estado del inquilino con la API de Google EMM. Los valores posibles son: `notBound`, `bound`, `boundAndValidated` y `unbinding`.|
|lastAppSyncDateTime|DateTimeOffset|Última hora de finalización para la sincronización de la aplicación|
|lastAppSyncStatus|[androidManagedStoreAccountAppSyncStatus](../resources/intune-androidforwork-androidmanagedstoreaccountappsyncstatus.md)|Resultado de la última sincronización de aplicación. Los valores posibles son: `success`, `credentialsNotValid`, `androidForWorkApiError`, `managementServiceError`, `unknownError`, `none`.|
|ownerUserPrincipalName|String|UPN del propietario que creó la empresa|
|ownerOrganizationName|String|Nombre de la organización utiliza cuando incorporación Enterprise Android|
|lastModifiedDateTime|DateTimeOffset|Hora de última modificación de la configuración de la empresa para Android|
|enrollmentTarget|[androidManagedStoreAccountEnrollmentTarget](../resources/intune-androidforwork-androidmanagedstoreaccountenrollmenttarget.md)|Indica qué usuarios pueden inscribirse dispositivos en administración de dispositivos Android empresariales. Los valores posibles son: `none`, `all`, `targeted` y `targetedAsEnrollmentRestrictions`.|
|targetGroupIds|Colección String|Especifica los grupos de AAD que pueden inscribir dispositivos en la administración de dispositivos de Android for Work si se establece enrollmentTarget en "Dirigido"|
|deviceOwnerManagementEnabled|Booleano|Indica si esta cuenta es flighting para la administración de propietario dispositivos Android con CloudDPC.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.androidManagedStoreAccountEnterpriseSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.androidManagedStoreAccountEnterpriseSettings",
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





