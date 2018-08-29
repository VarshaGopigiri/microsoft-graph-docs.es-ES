# <a name="update-androidlobapp"></a>Actualizar androidLobApp

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Actualice las propiedades de un objeto [androidLobApp](../resources/intune_apps_androidlobapp.md).
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso|Permisos (de más a menos privilegiados)|
|:---|:---|
|Delegado (cuenta profesional o educativa)|DeviceManagementApps.ReadWrite.All|
|Delegado (cuenta personal de Microsoft)|No admitida.|
|Aplicación|No admitida.|

## <a name="http-request"></a>Solicitud HTTP
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Authorization|Se requiere &lt;token&gt; de portador.|
|Aceptar|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, especifique una representación JSON del objeto [androidLobApp](../resources/intune_apps_androidlobapp.md).

En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [androidLobApp](../resources/intune_apps_androidlobapp.md).

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).|
|displayName|Cadena|Título de la aplicación importado o proporcionado por el administrador. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).|
|descripción|Cadena|Descripción de la aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).|
|publicador|Cadena|Publicador de la aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).|
|largeIcon|[mimeContent](../resources/intune_shared_mimecontent.md)|Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).|
|createdDateTime|DateTimeOffset|Fecha y hora de creación de la aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora de la última modificación de la aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).|
|isFeatured|Booleano|Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).|
|privacyInformationUrl|Cadena|La dirección URL de la declaración de privacidad. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).|
|informationUrl|Cadena|La dirección URL para obtener más información. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).|
|owner|Cadena|Propietario de la aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).|
|developer|Cadena|Desarrollador de la aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).|
|notas|Cadena|Notas de la aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).|
|publishingState|[mobileAppPublishingState](../resources/intune_apps_mobileapppublishingstate.md)|Estado de publicación de la aplicación. La aplicación no puede asignarse a menos que se publique. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md). Los valores posibles son: `notPublished`, `processing` y `published`.|
|committedContentVersion|Cadena|Versión interna del contenido confirmado. Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).|
|fileName|Cadena|Nombre del archivo de la aplicación de LOB principal. Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).|
|size|Int64|Tamaño total, incluidos todos los archivos cargados. Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).|
|packageId|Cadena|El identificador del paquete.|
|minimumSupportedOperatingSystem|[androidMinimumOperatingSystem](../resources/intune_apps_androidminimumoperatingsystem.md)|Valor del sistema operativo mínimo aplicable.|
|versionName|Cadena|El nombre de la versión de la aplicación de línea de negocio (LoB) de Android.|
|versionCode|Cadena|El código de versión de la aplicación de línea de negocio (LoB) de Android.|



## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [androidLobApp](../resources/intune_apps_androidlobapp.md) actualizado en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 1087

{
  "displayName": "Display Name value",
  "description": "Description value",
  "publisher": "Publisher value",
  "largeIcon": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "isFeatured": true,
  "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
  "informationUrl": "https://example.com/informationUrl/",
  "owner": "Owner value",
  "developer": "Developer value",
  "notes": "Notes value",
  "publishingState": "processing",
  "committedContentVersion": "Committed Content Version value",
  "fileName": "File Name value",
  "size": 4,
  "packageId": "Package Id value",
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.androidMinimumOperatingSystem",
    "v4_0": true,
    "v4_0_3": true,
    "v4_1": true,
    "v4_2": true,
    "v4_3": true,
    "v4_4": true,
    "v5_0": true,
    "v5_1": true
  },
  "versionName": "Version Name value",
  "versionCode": "Version Code value"
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1247

{
  "@odata.type": "#microsoft.graph.androidLobApp",
  "id": "4b9a27d0-27d0-4b9a-d027-9a4bd0279a4b",
  "displayName": "Display Name value",
  "description": "Description value",
  "publisher": "Publisher value",
  "largeIcon": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "isFeatured": true,
  "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
  "informationUrl": "https://example.com/informationUrl/",
  "owner": "Owner value",
  "developer": "Developer value",
  "notes": "Notes value",
  "publishingState": "processing",
  "committedContentVersion": "Committed Content Version value",
  "fileName": "File Name value",
  "size": 4,
  "packageId": "Package Id value",
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.androidMinimumOperatingSystem",
    "v4_0": true,
    "v4_0_3": true,
    "v4_1": true,
    "v4_2": true,
    "v4_3": true,
    "v4_4": true,
    "v5_0": true,
    "v5_1": true
  },
  "versionName": "Version Name value",
  "versionCode": "Version Code value"
}
```



