---
title: Tipo de recurso vppToken
description: Compra varias licencias para aplicaciones de aplicaciones iOS a través del programa de compras por volumen de Apple para la empresa o el ámbito educativo. Esto implica configurar una cuenta de Apple VPP desde el sitio web de Apple y cargar el token de Apple VPP empresarial o educativo en Intune. A continuación, puede sincronizar la información de compra por volumen con Intune y realizar un seguimiento de su uso de la aplicación de compra por volumen. Puede cargar varios token de Apple VPP empresarial o educativo.
ms.openlocfilehash: 48b7b455cc4e8af99ccfb33dfa5cc7c4a7989e15
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089321"
---
# <a name="vpptoken-resource-type"></a>Tipo de recurso vppToken

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Compra varias licencias para aplicaciones de aplicaciones iOS a través del programa de compras por volumen de Apple para la empresa o el ámbito educativo. Esto implica configurar una cuenta de Apple VPP desde el sitio web de Apple y cargar el token de Apple VPP empresarial o educativo en Intune. A continuación, puede sincronizar la información de compra por volumen con Intune y realizar un seguimiento de su uso de la aplicación de compra por volumen. Puede cargar varios token de Apple VPP empresarial o educativo.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar vppTokens](../api/intune-onboarding-vpptoken-list.md)|Colección [vppToken](../resources/intune-onboarding-vpptoken.md)|Enumera las propiedades y las relaciones de los objetos [vppToken](../resources/intune-onboarding-vpptoken.md).|
|[Obtener vppToken](../api/intune-onboarding-vpptoken-get.md)|[vppToken](../resources/intune-onboarding-vpptoken.md)|Lee las propiedades y las relaciones del objeto [vppToken](../resources/intune-onboarding-vpptoken.md).|
|[Crear vppToken](../api/intune-onboarding-vpptoken-create.md)|[vppToken](../resources/intune-onboarding-vpptoken.md)|Crea un nuevo objeto [vppToken](../resources/intune-onboarding-vpptoken.md).|
|[Eliminar vppToken](../api/intune-onboarding-vpptoken-delete.md)|Ninguno|Elimina un [vppToken](../resources/intune-onboarding-vpptoken.md).|
|[Actualizar vppToken](../api/intune-onboarding-vpptoken-update.md)|[vppToken](../resources/intune-onboarding-vpptoken.md)|Actualiza las propiedades de un objeto [vppToken](../resources/intune-onboarding-vpptoken.md).|
|[Acción syncLicenses](../api/intune-onboarding-vpptoken-synclicenses.md)|[vppToken](../resources/intune-onboarding-vpptoken.md)|Sincroniza las licencias asociadas con un determinado appleVolumePurchaseProgramToken.|
|[acción revokeLicenses](../api/intune-onboarding-vpptoken-revokelicenses.md)|Ninguno|Revocar licencias asociadas con un appleVolumePurchaseProgramToken específico|
|[getLicensesForApp (función)](../api/intune-onboarding-vpptoken-getlicensesforapp.md)|colección de [vppTokenLicenseSummary](../resources/intune-onboarding-vpptokenlicensesummary.md)|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Esto se genera automáticamente cuando se crea el appleVolumePurchaseProgramToken. Es la clave de la entidad.|
|organizationName|Cadena|Organización asociada al token del Programa de Compras por Volumen de Apple|
|vppTokenAccountType|[vppTokenAccountType](../resources/intune-shared-vpptokenaccounttype.md)|Tipo de programa de compras por volumen al que está asociado el token del Programa de Compras por Volumen de Apple especificado. Los valores posibles son: `business` y `education`. Los valores posibles son: `business` y `education`.|
|Id. de Apple|Cadena|Identificador de Apple asociado al token del Programa de compras por volumen de Apple especificado.|
|expirationDateTime|DateTimeOffset|La fecha y hora de vencimiento del token del Programa de compras por volumen de Apple.|
|lastSyncDateTime|DateTimeOffset|La última vez que se realizó la sincronización de una aplicación con el servicio del programa de compras por volumen de Apple utilizando el token de ese programa de compras.|
|token|Cadena|La cadena del token del programa de compras por volumen de Apple descargada desde ese programa de compras.|
|lastModifiedDateTime|DateTimeOffset|La fecha y hora de modificación asociada con el token del Programa de compras por volumen de Apple.|
|estado|[vppTokenState](../resources/intune-onboarding-vpptokenstate.md)|Estado actual del token del Programa de compras por volumen de Apple. Los valores posibles son: `unknown`, `valid`, `expired`, `invalid` y `assignedToExternalMDM`. Los valores posibles son: `unknown`, `valid`, `expired`, `invalid` y `assignedToExternalMDM`.|
|tokenActionResults|colección de [vppTokenActionResult](../resources/intune-onboarding-vpptokenactionresult.md)|La colección de Estados de las acciones que se realiza en el Token de programa de compra de Apple por volumen.|
|lastSyncStatus|[vppTokenSyncStatus](../resources/intune-onboarding-vpptokensyncstatus.md)|Estado de sincronización actual de la última sincronización de la aplicación que se activó con el Token del programa de compras por volumen de Apple. Los valores posibles son: `none`, `inProgress`, `completed` y `failed`. Los valores posibles son: `none`, `inProgress`, `completed` y `failed`.|
|automaticallyUpdateApps|Booleano|Si las aplicaciones para el token VPP se actualizarán automáticamente o no.|
|countryOrRegion|Cadena|Si las aplicaciones para el token VPP se actualizarán automáticamente o no.|
|dataSharingConsentGranted|Booleano|Concede de consentimiento para uso compartido con el programa de compra de Apple por volumen de datos.|
|displayName|String|Un administrador especifica el nombre descriptivo del token.|
|locationName|String|Ubicación de token devuelto desde VPP de Apple.|
|claimTokenManagementFromExternalMdm|Booleano|Administración de consentimiento para permitir que afirma token administración de MDM. externo|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.vppToken"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.vppToken",
  "id": "String (identifier)",
  "organizationName": "String",
  "vppTokenAccountType": "String",
  "appleId": "String",
  "expirationDateTime": "String (timestamp)",
  "lastSyncDateTime": "String (timestamp)",
  "token": "String",
  "lastModifiedDateTime": "String (timestamp)",
  "state": "String",
  "tokenActionResults": [
    {
      "@odata.type": "microsoft.graph.vppTokenActionResult",
      "actionName": "String",
      "actionState": "String",
      "startDateTime": "String (timestamp)",
      "lastUpdatedDateTime": "String (timestamp)"
    }
  ],
  "lastSyncStatus": "String",
  "automaticallyUpdateApps": true,
  "countryOrRegion": "String",
  "dataSharingConsentGranted": true,
  "displayName": "String",
  "locationName": "String",
  "claimTokenManagementFromExternalMdm": true
}
```





