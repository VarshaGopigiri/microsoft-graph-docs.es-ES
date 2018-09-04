# <a name="vpptoken-resource-type"></a>Tipo de recurso vppToken

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Compra varias licencias para aplicaciones de aplicaciones iOS a través del programa de compras por volumen de Apple para la empresa o el ámbito educativo. Esto implica configurar una cuenta de Apple VPP desde el sitio web de Apple y cargar el token de Apple VPP empresarial o educativo en Intune. A continuación, puede sincronizar la información de compra por volumen con Intune y realizar un seguimiento de su uso de la aplicación de compra por volumen. Puede cargar varios token de Apple VPP empresarial o educativo.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar vppTokens](../api/intune_onboarding_vpptoken_list.md)|Colección [vppToken](../resources/intune_onboarding_vpptoken.md)|Enumera las propiedades y las relaciones de los objetos [vppToken](../resources/intune_onboarding_vpptoken.md).|
|[Obtener vppToken](../api/intune_onboarding_vpptoken_get.md)|[vppToken](../resources/intune_onboarding_vpptoken.md)|Lee las propiedades y las relaciones del objeto [vppToken](../resources/intune_onboarding_vpptoken.md).|
|[Crear vppToken](../api/intune_onboarding_vpptoken_create.md)|[vppToken](../resources/intune_onboarding_vpptoken.md)|Crea un nuevo objeto [vppToken](../resources/intune_onboarding_vpptoken.md).|
|[Eliminar vppToken](../api/intune_onboarding_vpptoken_delete.md)|Ninguno|Elimina un [vppToken](../resources/intune_onboarding_vpptoken.md).|
|[Actualizar vppToken](../api/intune_onboarding_vpptoken_update.md)|[vppToken](../resources/intune_onboarding_vpptoken.md)|Actualiza las propiedades de un objeto [vppToken](../resources/intune_onboarding_vpptoken.md).|
|[Acción syncLicenses](../api/intune_onboarding_vpptoken_synclicenses.md)|[vppToken](../resources/intune_onboarding_vpptoken.md)|Sincroniza las licencias asociadas con un determinado appleVolumePurchaseProgramToken.|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Esto se genera automáticamente cuando se crea el appleVolumePurchaseProgramToken. Es la clave de la entidad.|
|organizationName|Cadena|Organización asociada al token del Programa de Compras por Volumen de Apple|
|vppTokenAccountType|[vppTokenAccountType](../resources/intune_shared_vpptokenaccounttype.md)|Tipo de programa de compras por volumen al que está asociado el token del programa de compras por volumen de Apple especificado. Los valores posibles son: `business` y `education`. Los valores posibles son: `business` y `education`.|
|appleId|Cadena|Identificador de Apple asociado al token del Programa de compras por volumen de Apple especificado.|
|expirationDateTime|DateTimeOffset|La fecha y hora de vencimiento del token del Programa de compras por volumen de Apple.|
|lastSyncDateTime|DateTimeOffset|La última vez que se realizó la sincronización de una aplicación con el servicio del programa de compras por volumen de Apple utilizando el token de ese programa de compras.|
|token|Cadena|La cadena del token del programa de compras por volumen de Apple descargada desde ese programa de compras.|
|lastModifiedDateTime|DateTimeOffset|La fecha y hora de modificación asociada con el token del Programa de compras por volumen de Apple.|
|state|[vppTokenState](../resources/intune_onboarding_vpptokenstate.md)|Estado actual del token del programa de compras por volumen de Apple. Los valores posibles son: `unknown`, `valid`, `expired` y `invalid`. Los valores posibles son: `unknown`, `valid`, `expired` y `invalid`.|
|lastSyncStatus|[vppTokenSyncStatus](../resources/intune_onboarding_vpptokensyncstatus.md)|Estado de sincronización actual de la última sincronización de la aplicación que se activó usando el token del programa de compras por volumen de Apple. Los valores posibles son: `none`, `inProgress`, `completed` y `failed`. Los valores posibles son: `none`, `inProgress`, `completed` y `failed`.|
|automaticallyUpdateApps|Booleano|Si las aplicaciones para el token VPP se actualizarán automáticamente o no.|
|countryOrRegion|Cadena|Si las aplicaciones para el token VPP se actualizarán automáticamente o no.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
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
  "lastSyncStatus": "String",
  "automaticallyUpdateApps": true,
  "countryOrRegion": "String"
}
```



