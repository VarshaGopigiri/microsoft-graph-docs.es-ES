# <a name="microsoftstoreforbusinessapp-resource-type"></a>Tipo de recurso microsoftStoreForBusinessApp

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Aplicación de Microsoft Store para Empresas. Esta clase no es compatible con Crear, Eliminar ni Actualizar.

Hereda de [mobileApp](../resources/intune_apps_mobileapp.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar microsoftStoreForBusinessApps](../api/intune_apps_microsoftstoreforbusinessapp_list.md)|Colección [microsoftStoreForBusinessApp](../resources/intune_apps_microsoftstoreforbusinessapp.md)|Enumere las propiedades y las relaciones de los objetos [microsoftStoreForBusinessApp](../resources/intune_apps_microsoftstoreforbusinessapp.md).|
|[Obtener microsoftStoreForBusinessApp](../api/intune_apps_microsoftstoreforbusinessapp_get.md)|[microsoftStoreForBusinessApp](../resources/intune_apps_microsoftstoreforbusinessapp.md)|Lea las propiedades y las relaciones del objeto [microsoftStoreForBusinessApp](../resources/intune_apps_microsoftstoreforbusinessapp.md).|
|[Crear microsoftStoreForBusinessApp](../api/intune_apps_microsoftstoreforbusinessapp_create.md)|[microsoftStoreForBusinessApp](../resources/intune_apps_microsoftstoreforbusinessapp.md)|Cree un objeto [microsoftStoreForBusinessApp](../resources/intune_apps_microsoftstoreforbusinessapp.md).|
|[Eliminar microsoftStoreForBusinessApp](../api/intune_apps_microsoftstoreforbusinessapp_delete.md)|Ninguna|Elimina un [microsoftStoreForBusinessApp](../resources/intune_apps_microsoftstoreforbusinessapp.md).|
|[Actualizar microsoftStoreForBusinessApp](../api/intune_apps_microsoftstoreforbusinessapp_update.md)|[microsoftStoreForBusinessApp](../resources/intune_apps_microsoftstoreforbusinessapp.md)|Actualice las propiedades de un objeto [microsoftStoreForBusinessApp](../resources/intune_apps_microsoftstoreforbusinessapp.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).|
|displayName|Cadena|Título de la aplicación importado o proporcionado por el administrador. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).|
|descripción|Cadena|Descripción de la aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).|
|publicador|Cadena|Publicador de la aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).|
|largeIcon|[mimeContent](../resources/intune_shared_mimecontent.md)|Icono grande que se mostrará en los detalles de la aplicación y se usa para cargar el icono. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).|
|createdDateTime|DateTimeOffset|Fecha y hora de creación de la aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora de la última modificación de la aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).|
|isFeatured|Booleano|El valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|privacyInformationUrl|Cadena|La dirección URL de la declaración de privacidad. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).|
|informationUrl|Cadena|La dirección URL para obtener más información. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).|
|propietario|Cadena|Propietario de la aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).|
|desarrollador|Cadena|Desarrollador de la aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).|
|notas|Cadena|Notas de la aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).|
|publishingState|[mobileAppPublishingState](../resources/intune_apps_mobileapppublishingstate.md)|Estado de publicación de la aplicación. La aplicación no puede asignarse a menos que se publique. Se hereda de [mobileApp](../resources/intune_apps_mobileapp.md). Los valores posibles son: `notPublished`, `processing` y `published`.|
|usedLicenseCount|Int32|Número de licencias de Microsoft Store para Empresas en uso.|
|totalLicenseCount|Int32|Número total de licencias de Microsoft Store para Empresas.|
|productKey|String|Clave de producto de la aplicación|
|licenseType|[microsoftStoreForBusinessLicenseType](../resources/intune_apps_microsoftstoreforbusinesslicensetype.md)|El tipo de licencia de la aplicación. Los valores posibles son: `offline` y `online`.|
|packageIdentityName|String|El identificador del paquete de aplicación.|

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
  "@odata.type": "microsoft.graph.microsoftStoreForBusinessApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.microsoftStoreForBusinessApp",
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
  "productKey": "String",
  "licenseType": "String",
  "packageIdentityName": "String"
}
```



