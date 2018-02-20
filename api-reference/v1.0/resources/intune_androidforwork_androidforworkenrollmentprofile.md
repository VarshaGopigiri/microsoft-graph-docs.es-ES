# <a name="androidforworkenrollmentprofile-resource-type"></a>Tipo de recurso androidForWorkEnrollmentProfile

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Perfil de inscripción usado al inscribir dispositivos COSU mediante la administración en la nube de Google.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar androidForWorkEnrollmentProfiles](../api/intune_androidforwork_androidforworkenrollmentprofile_list.md)|Colección [androidForWorkEnrollmentProfile](../resources/intune_androidforwork_androidforworkenrollmentprofile.md)|Enumere las propiedades y las relaciones de los objetos [androidForWorkEnrollmentProfile](../resources/intune_androidforwork_androidforworkenrollmentprofile.md).|
|[Obtener androidForWorkEnrollmentProfile](../api/intune_androidforwork_androidforworkenrollmentprofile_get.md)|[androidForWorkEnrollmentProfile](../resources/intune_androidforwork_androidforworkenrollmentprofile.md)|Lea las propiedades y las relaciones del objeto [androidForWorkEnrollmentProfile](../resources/intune_androidforwork_androidforworkenrollmentprofile.md).|
|[Crear androidForWorkEnrollmentProfile](../api/intune_androidforwork_androidforworkenrollmentprofile_create.md)|[androidForWorkEnrollmentProfile](../resources/intune_androidforwork_androidforworkenrollmentprofile.md)|Cree un objeto [androidForWorkEnrollmentProfile](../resources/intune_androidforwork_androidforworkenrollmentprofile.md).|
|[Eliminar androidForWorkEnrollmentProfile](../api/intune_androidforwork_androidforworkenrollmentprofile_delete.md)|Ninguna|Elimina un [androidForWorkEnrollmentProfile](../resources/intune_androidforwork_androidforworkenrollmentprofile.md).|
|[Actualizar androidForWorkEnrollmentProfile](../api/intune_androidforwork_androidforworkenrollmentprofile_update.md)|[androidForWorkEnrollmentProfile](../resources/intune_androidforwork_androidforworkenrollmentprofile.md)|Actualice las propiedades de un objeto [androidForWorkEnrollmentProfile](../resources/intune_androidforwork_androidforworkenrollmentprofile.md).|
|[Acción revokeToken](../api/intune_androidforwork_androidforworkenrollmentprofile_revoketoken.md)|Ninguna|Todavía no documentado|
|[Acción createToken](../api/intune_androidforwork_androidforworkenrollmentprofile_createtoken.md)|Ninguna|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|accountId|Cadena|El GUID del espacio empresarial al que pertenece el perfil de inscripción.|
|id|Cadena|GUID único para el perfil de inscripción.|
|nombre|Cadena|(En desuso) Nombre para mostrar del perfil de inscripción.|
|displayName|Cadena|Nombre para mostrar del perfil de inscripción.|
|descripción|Cadena|Descripción del perfil de inscripción.|
|createdDateTime|DateTimeOffset|Fecha y hora en que se creó el perfil de inscripción.|
|modifiedDateTime|DateTimeOffset|(En desuso) Fecha y hora en que se modificó el perfil de inscripción por última vez.|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en que se modificó el perfil de inscripción por última vez.|
|tokenValue|Cadena|Valor del token creado más recientemente para este perfil de inscripción.|
|tokenExpirationDateTime|DateTimeOffset|Fecha y hora en que caducará el token creado más recientemente.|
|totalEnrollmentCount|Int32|(En desuso) Número total de dispositivos Android que se han inscrito con este perfil de inscripción.|
|enrolledDeviceCount|Int32|Número total de dispositivos Android que se han inscrito con este perfil de inscripción.|
|qrCode|Cadena|(En desuso) Cadena usada para generar un código QR para el token.|
|qrCodeContent|Cadena|Cadena usada para generar un código QR para el token.|
|qrCodeImage|[mimeContent](../resources/intune_androidforwork_mimecontent.md)|Cadena usada para generar un código QR para el token.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.androidForWorkEnrollmentProfile"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.androidForWorkEnrollmentProfile",
  "accountId": "String",
  "id": "String (identifier)",
  "name": "String",
  "displayName": "String",
  "description": "String",
  "createdDateTime": "String (timestamp)",
  "modifiedDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "tokenValue": "String",
  "tokenExpirationDateTime": "String (timestamp)",
  "totalEnrollmentCount": 1024,
  "enrolledDeviceCount": 1024,
  "qrCode": "String",
  "qrCodeContent": "String",
  "qrCodeImage": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "String",
    "value": "binary"
  }
}
```



