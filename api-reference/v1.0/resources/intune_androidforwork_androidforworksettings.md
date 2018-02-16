# <a name="androidforworksettings-resource-type"></a>Tipo de recurso androidForWorkSettings

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Configuración de Android for Work
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener androidForWorkSettings](../api/intune_androidforwork_androidforworksettings_get.md)|[androidForWorkSettings](../resources/intune_androidforwork_androidforworksettings.md)|Lea las propiedades y las relaciones del objeto [androidForWorkSettings](../resources/intune_androidforwork_androidforworksettings.md).|
|[Actualizar androidForWorkSettings](../api/intune_androidforwork_androidforworksettings_update.md)|[androidForWorkSettings](../resources/intune_androidforwork_androidforworksettings.md)|Actualice las propiedades de un objeto [androidForWorkSettings](../resources/intune_androidforwork_androidforworksettings.md).|
|[Acción requestSignupUrl](../api/intune_androidforwork_androidforworksettings_requestsignupurl.md)|cadena|Genera una dirección URL de inicio de sesión que se utiliza para registrarse en la administración de Android for Work.|
|[Acción completeSignup](../api/intune_androidforwork_androidforworksettings_completesignup.md)|Ninguna|Completa el flujo de registro para la administración de Android for Work.|
|[Acción syncApps](../api/intune_androidforwork_androidforworksettings_syncapps.md)|Ninguna|Sincroniza las aplicaciones aprobadas para la empresa.|
|[Acción unbind](../api/intune_androidforwork_androidforworksettings_unbind.md)|Ninguna|Deshabilita la administración de Android for Work para la empresa.|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|cadena|El identificador de la configuración de Android for Work|
|bindStatus|cadena|Estado de enlace del espacio empresarial con la API del EMM de Google. Los valores posibles son: `notBound`, `bound`, `boundAndValidated` y `unbinding`.|
|lastAppSyncDateTime|DateTimeOffset|Última hora de finalización para la sincronización de la aplicación|
|lastAppSyncStatus|cadena|Resultado de la última sincronización de la aplicación. Los valores posibles son: `success`, `credentialsNotValid`, `androidForWorkApiError`, `managementServiceError`, `unknownError` y `none`.|
|ownerUserPrincipalName|cadena|UPN del propietario que creó la empresa|
|ownerOrganizationName|cadena|Nombre de organización usado al incorporar Android for Work|
|lastModifiedDateTime|DateTimeOffset|Última hora de modificación para la configuración de Android for Work|
|enrollmentTarget|cadena|Indica qué usuarios pueden inscribir dispositivos en la administración de dispositivos de Android for Work. Los valores posibles son: `none`, `all`, `targeted` y `targetedAsEnrollmentRestrictions`.|
|targetGroupIds|Colección de cadenas|Especifica qué grupos de AAD pueden inscribir dispositivos en la administración de dispositivos de Android for Work si se establece enrollmentTarget en "Dirigido"|

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
  ]
}
```



