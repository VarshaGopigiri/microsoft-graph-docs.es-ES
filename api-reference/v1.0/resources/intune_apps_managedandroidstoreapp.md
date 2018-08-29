# <a name="managedandroidstoreapp-resource-type"></a>Tipo de recurso managedAndroidStoreApp

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades y las propiedades heredadas para las aplicaciones de la tienda Android que puede administrar con una directiva de protección de aplicaciones de Intune.

Hereda de [managedApp](../resources/intune_apps_managedapp.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar managedAndroidStoreApps](../api/intune_apps_managedandroidstoreapp_list.md)|Colección [managedAndroidStoreApp](../resources/intune_apps_managedandroidstoreapp.md)|Enumere las propiedades y las relaciones de los objetos [managedAndroidStoreApp](../resources/intune_apps_managedandroidstoreapp.md).|
|[Obtener managedAndroidStoreApp](../api/intune_apps_managedandroidstoreapp_get.md)|[managedAndroidStoreApp](../resources/intune_apps_managedandroidstoreapp.md)|Lea las propiedades y las relaciones del objeto [managedAndroidStoreApp](../resources/intune_apps_managedandroidstoreapp.md).|
|[Crear managedAndroidStoreApp](../api/intune_apps_managedandroidstoreapp_create.md)|[managedAndroidStoreApp](../resources/intune_apps_managedandroidstoreapp.md)|Cree un objeto [managedAndroidStoreApp](../resources/intune_apps_managedandroidstoreapp.md).|
|[Eliminar managedAndroidStoreApp](../api/intune_apps_managedandroidstoreapp_delete.md)|Ninguna|Elimina un [managedAndroidStoreApp](../resources/intune_apps_managedandroidstoreapp.md).|
|[Actualizar managedAndroidStoreApp](../api/intune_apps_managedandroidstoreapp_update.md)|[managedAndroidStoreApp](../resources/intune_apps_managedandroidstoreapp.md)|Actualice las propiedades de un objeto [managedAndroidStoreApp](../resources/intune_apps_managedandroidstoreapp.md).|

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
|isFeatured|Booleano|Valor que indica si el administrador ha marcado la aplicación como destacada. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).|
|privacyInformationUrl|Cadena|La dirección URL de la declaración de privacidad. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).|
|informationUrl|Cadena|La dirección URL para obtener más información. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).|
|owner|Cadena|Propietario de la aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).|
|developer|Cadena|Desarrollador de la aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).|
|notas|Cadena|Notas de la aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md).|
|publishingState|[mobileAppPublishingState](../resources/intune_apps_mobileapppublishingstate.md)|Estado de publicación de la aplicación. La aplicación no puede asignarse a menos que se publique. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md). Los valores posibles son: `notPublished`, `processing` y `published`.|
|appAvailability|[managedAppAvailability](../resources/intune_apps_managedappavailability.md)|Disponibilidad de la aplicación. Heredado de [managedApp](../resources/intune_apps_managedapp.md). Los valores posibles son: `global`, `lineOfBusiness`.|
|version|Cadena|Versión de la aplicación. Heredado de [managedApp](../resources/intune_apps_managedapp.md)|
|packageId|Cadena|El identificador de paquete de la aplicación.|
|appStoreUrl|Cadena|La AppStoreUrl de Android.|
|minimumSupportedOperatingSystem|[androidMinimumOperatingSystem](../resources/intune_apps_androidminimumoperatingsystem.md)|El valor para el sistema operativo mínimo compatible.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|categorías|Colección [mobileAppCategory](../resources/intune_apps_mobileappcategory.md)|La lista de categorías para esta aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|asignaciones|Colección [mobileAppAssignment](../resources/intune_apps_mobileappassignment.md)|La lista de asignaciones de grupo para esta aplicación móvil. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "keyProperty": "id",
  "baseType": "microsoft.graph.managedApp",
  "@odata.type": "microsoft.graph.managedAndroidStoreApp"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAndroidStoreApp",
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
  "appAvailability": "String",
  "version": "String",
  "packageId": "String",
  "appStoreUrl": "String",
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
  }
}
```



