# <a name="iosvppapp-resource-type"></a>Tipo de recurso iosVppApp

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades y las propiedades heredadas de las aplicaciones del Programa de Compras por Volumen (VPP) de iOS.

Hereda de [mobileApp](../resources/intune_apps_mobileapp.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar iosVppApps](../api/intune_apps_iosvppapp_list.md)|Colección [iosVppApp](../resources/intune_apps_iosvppapp.md)|Enumere las propiedades y las relaciones de los objetos [iosVppApp](../resources/intune_apps_iosvppapp.md).|
|[Obtener iosVppApp](../api/intune_apps_iosvppapp_get.md)|[iosVppApp](../resources/intune_apps_iosvppapp.md)|Lea las propiedades y las relaciones del objeto [iosVppApp](../resources/intune_apps_iosvppapp.md).|
|[Crear iosVppApp](../api/intune_apps_iosvppapp_create.md)|[iosVppApp](../resources/intune_apps_iosvppapp.md)|Cree un objeto [iosVppApp](../resources/intune_apps_iosvppapp.md).|
|[Eliminar iosVppApp](../api/intune_apps_iosvppapp_delete.md)|Ninguna|Elimina un [iosVppApp](../resources/intune_apps_iosvppapp.md).|
|[Actualizar iosVppApp](../api/intune_apps_iosvppapp_update.md)|[iosVppApp](../resources/intune_apps_iosvppapp.md)|Actualice las propiedades de un objeto [iosVppApp](../resources/intune_apps_iosvppapp.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|displayName|Cadena|El título de la aplicación importado o proporcionado por el administrador. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|descripción|Cadena|La descripción de la aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|publicador|Cadena|El publicador de la aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|largeIcon|[mimeContent](../resources/intune_apps_mimecontent.md)|El icono grande, se muestra en los detalles de la aplicación y se usa para cargar el icono. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|createdDateTime|DateTimeOffset|La fecha y la hora de creación de la aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora de la última modificación de la aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|isFeatured|Booleano|El valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|privacyInformationUrl|Cadena|La dirección URL de la declaración de privacidad. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|informationUrl|Cadena|La dirección URL para obtener más información. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|propietario|Cadena|Propietario de la aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|desarrollador|Cadena|El desarrollador de la aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|notas|Cadena|Notas de la aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|publishingState|Cadena|El estado de publicación de la aplicación. La aplicación no puede asignarse a menos que se publique. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md). Los valores posibles son: `notPublished`, `processing` y `published`.|
|usedLicenseCount|Int32|El número de licencias de VPP en uso.|
|totalLicenseCount|Int32|El número total de licencias de VPP.|
|releaseDateTime|DateTimeOffset|La fecha y hora de publicación de la aplicación de VPP.|
|appStoreUrl|Cadena|La dirección URL de la tienda.|
|licensingType|[vppLicensingType](../resources/intune_apps_vpplicensingtype.md)|El tipo de licencia compatible.|
|applicableDeviceType|[iosDeviceType](../resources/intune_apps_iosdevicetype.md)|El tipo de dispositivo iOS aplicable.|
|vppTokenOrganizationName|Cadena|La organización asociada con el token del Programa de Compras por Volumen de Apple|
|vppTokenAccountType|Cadena|El tipo de programa de compras por volumen al que está asociado el token del Programa de Compras por Volumen de Apple especificado. Los valores posibles son: `business` y `education`. Los valores posibles son: `business` y `education`.|
|vppTokenAppleId|Cadena|El Id. de Apple asociado con el token del Programa de Compras por Volumen de Apple especificado.|
|bundleId|Cadena|El nombre de la identidad.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|categorías|Colección [mobileAppCategory](../resources/intune_apps_mobileappcategory.md)|La lista de categorías para esta aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|asignaciones|Colección [mobileAppAssignment](../resources/intune_apps_mobileappassignment.md)|La lista de asignaciones de grupo para esta aplicación móvil. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.iosVppApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosVppApp",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "publisher": "String",
  "largeIcon": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "String",
    "value": "binary"
  },
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "isFeatured": true,
  "privacyInformationUrl": "String",
  "informationUrl": "String",
  "owner": "String",
  "developer": "String",
  "notes": "String",
  "publishingState": "String",
  "usedLicenseCount": 1024,
  "totalLicenseCount": 1024,
  "releaseDateTime": "String (timestamp)",
  "appStoreUrl": "String",
  "licensingType": {
    "@odata.type": "microsoft.graph.vppLicensingType",
    "supportsUserLicensing": true,
    "supportsDeviceLicensing": true
  },
  "applicableDeviceType": {
    "@odata.type": "microsoft.graph.iosDeviceType",
    "iPad": true,
    "iPhoneAndIPod": true
  },
  "vppTokenOrganizationName": "String",
  "vppTokenAccountType": "String",
  "vppTokenAppleId": "String",
  "bundleId": "String"
}
```



