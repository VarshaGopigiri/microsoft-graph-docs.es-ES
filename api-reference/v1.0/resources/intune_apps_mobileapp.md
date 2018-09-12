# <a name="mobileapp-resource-type"></a>Tipo de recurso mobileApp

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Una clase abstracta que contiene las propiedades base para las aplicaciones móviles de Intune.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar mobileApps](../api/intune_apps_mobileapp_list.md)|Colección [mobileApp](../resources/intune_apps_mobileapp.md)|Enumere las propiedades y las relaciones de los objetos [mobileApp](../resources/intune_apps_mobileapp.md).|
|[Obtener mobileApp](../api/intune_apps_mobileapp_get.md)|[mobileApp](../resources/intune_apps_mobileapp.md)|Lea las propiedades y las relaciones del objeto [mobileApp](../resources/intune_apps_mobileapp.md).|
|[Acción assign](../api/intune_apps_mobileapp_assign.md)|Ninguna|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad.|
|displayName|Cadena|El título de la aplicación importado o proporcionado por el administrador.|
|description|Cadena|La descripción de la aplicación.|
|publisher|Cadena|El publicador de la aplicación.|
|largeIcon|[mimeContent](../resources/intune_shared_mimecontent.md)|El icono grande, se muestra en los detalles de la aplicación y se usa para cargar el icono.|
|createdDateTime|DateTimeOffset|La fecha y la hora de creación de la aplicación.|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora de la última modificación de la aplicación.|
|isFeatured|Booleano|El valor que indica si el administrador ha marcado la aplicación como destacada.|
|privacyInformationUrl|Cadena|La dirección URL de la declaración de privacidad.|
|informationUrl|Cadena|La dirección URL para obtener más información.|
|propietario|Cadena|Propietario de la aplicación.|
|desarrollador|Cadena|El desarrollador de la aplicación.|
|notes|Cadena|Notas de la aplicación.|
|publishingState|[mobileAppPublishingState](../resources/intune_apps_mobileapppublishingstate.md)|El estado de publicación para la aplicación. La aplicación no se puede asignar a menos que se publique la aplicación. Los valores posibles son: `notPublished`, `processing`, `published`.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|categorías|Colección [mobileAppCategory](../resources/intune_apps_mobileappcategory.md)|La lista de categorías para esta aplicación.|
|asignaciones|Colección [mobileAppAssignment](../resources/intune_apps_mobileappassignment.md)|La lista de asignaciones de grupo para esta aplicación móvil.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.mobileApp"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileApp",
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
  "publishingState": "String"
}
```








