# <a name="webapp-resource-type"></a>Tipo de recurso webApp

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene propiedades y propiedades heredadas de aplicaciones web.

Hereda de [mobileApp](../resources/intune_apps_mobileapp.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar webApps](../api/intune_apps_webapp_list.md)|Colección [webApp](../resources/intune_apps_webapp.md)|Enumere las propiedades y las relaciones de los objetos [webApp](../resources/intune_apps_webapp.md).|
|[Obtener webApp](../api/intune_apps_webapp_get.md)|[webApp](../resources/intune_apps_webapp.md)|Lea las propiedades y las relaciones del objeto [webApp](../resources/intune_apps_webapp.md).|
|[Crear webApp](../api/intune_apps_webapp_create.md)|[webApp](../resources/intune_apps_webapp.md)|Cree un objeto [webApp](../resources/intune_apps_webapp.md).|
|[Eliminar webApp](../api/intune_apps_webapp_delete.md)|Ninguna|Elimina un [webApp](../resources/intune_apps_webapp.md).|
|[Actualizar webApp](../api/intune_apps_webapp_update.md)|[webApp](../resources/intune_apps_webapp.md)|Actualice las propiedades de un objeto [webApp](../resources/intune_apps_webapp.md).|

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
|publishingState|[mobileAppPublishingState](../resources/intune_apps_mobileapppublishingstate.md)|El estado de publicación de la aplicación. La aplicación no puede asignarse a menos que se publique. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md). Los valores posibles son: `notPublished`, `processing` y `published`.|
|appUrl|Cadena|Dirección URL de la aplicación web.|
|useManagedBrowser|Booleano|Indica si se va a usar el explorador administrado. Esta propiedad solo es aplicable a iOS y Android.|

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
  "baseType": "microsoft.graph.mobileApp",
  "@odata.type": "microsoft.graph.webApp"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.webApp",
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
  "appUrl": "String",
  "useManagedBrowser": true
}
```



