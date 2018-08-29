# <a name="update-macosofficesuiteapp"></a>Actualizar macOSOfficeSuiteApp

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Actualice las propiedades de un objeto [macOSOfficeSuiteApp](../resources/intune_apps_macosofficesuiteapp.md).
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
En el cuerpo de la solicitud, especifique una representación JSON del objeto [macOSOfficeSuiteApp](../resources/intune_apps_macosofficesuiteapp.md).

En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [macOSOfficeSuiteApp](../resources/intune_apps_macosofficesuiteapp.md).

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



## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [macOSOfficeSuiteApp](../resources/intune_apps_macosofficesuiteapp.md) actualizado en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 590

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
  "publishingState": "processing"
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 756

{
  "@odata.type": "#microsoft.graph.macOSOfficeSuiteApp",
  "id": "bf39e35d-e35d-bf39-5de3-39bf5de339bf",
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
  "publishingState": "processing"
}
```



