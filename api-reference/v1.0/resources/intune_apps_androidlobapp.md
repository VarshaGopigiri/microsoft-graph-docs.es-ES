# <a name="androidlobapp-resource-type"></a>Tipo de recurso androidLobApp

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene propiedades y propiedades heredadas de aplicaciones de línea de negocio de Android.

Hereda de [mobileLobApp](../resources/intune_apps_mobilelobapp.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar androidLobApps](../api/intune_apps_androidlobapp_list.md)|Colección [androidLobApp](../resources/intune_apps_androidlobapp.md)|Enumere las propiedades y las relaciones de los objetos [androidLobApp](../resources/intune_apps_androidlobapp.md).|
|[Obtener androidLobApp](../api/intune_apps_androidlobapp_get.md)|[androidLobApp](../resources/intune_apps_androidlobapp.md)|Lea las propiedades y las relaciones del objeto [androidLobApp](../resources/intune_apps_androidlobapp.md).|
|[Crear androidLobApp](../api/intune_apps_androidlobapp_create.md)|[androidLobApp](../resources/intune_apps_androidlobapp.md)|Cree un objeto [androidLobApp](../resources/intune_apps_androidlobapp.md).|
|[Eliminar androidLobApp](../api/intune_apps_androidlobapp_delete.md)|Ninguna|Elimina un [androidLobApp](../resources/intune_apps_androidlobapp.md).|
|[Actualizar androidLobApp](../api/intune_apps_androidlobapp_update.md)|[androidLobApp](../resources/intune_apps_androidlobapp.md)|Actualice las propiedades de un objeto [androidLobApp](../resources/intune_apps_androidlobapp.md).|

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
|committedContentVersion|Cadena|Versión interna del contenido confirmado. Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).|
|fileName|Cadena|Nombre del archivo de la aplicación de LOB principal. Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).|
|size|Int64|Tamaño total, incluidos todos los archivos cargados. Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md).|
|packageId|Cadena|El identificador del paquete.|
|minimumSupportedOperatingSystem|[androidMinimumOperatingSystem](../resources/intune_apps_androidminimumoperatingsystem.md)|Valor del sistema operativo mínimo aplicable.|
|versionName|Cadena|El nombre de la versión de la aplicación de línea de negocio (LoB) de Android.|
|versionCode|Cadena|El código de versión de la aplicación de línea de negocio (LoB) de Android.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|categorías|Colección [mobileAppCategory](../resources/intune_apps_mobileappcategory.md)|La lista de categorías para esta aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|asignaciones|Colección [mobileAppAssignment](../resources/intune_apps_mobileappassignment.md)|La lista de asignaciones de grupo para esta aplicación móvil. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|contentVersions|Colección [mobileAppContent](../resources/intune_apps_mobileappcontent.md)|La lista de versiones de contenido de esta aplicación. Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md)|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "keyProperty": "id",
  "baseType": "microsoft.graph.mobileLobApp",
  "@odata.type": "microsoft.graph.androidLobApp"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.androidLobApp",
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
  "committedContentVersion": "String",
  "fileName": "String",
  "size": 1024,
  "packageId": "String",
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
  "versionName": "String",
  "versionCode": "String"
}
```



