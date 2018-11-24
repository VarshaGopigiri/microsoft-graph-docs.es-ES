# <a name="macosofficesuiteapp-resource-type"></a>Tipo de recurso macOSOfficeSuiteApp

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene propiedades y propiedades heredadas de la aplicación del conjunto de aplicaciones de Office para macOS.

Hereda de [mobileApp](../resources/intune_apps_mobileapp.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar macOSOfficeSuiteApps](../api/intune_apps_macosofficesuiteapp_list.md)|Colección [macOSOfficeSuiteApp](../resources/intune_apps_macosofficesuiteapp.md)|Enumere las propiedades y las relaciones de los objetos [macOSOfficeSuiteApp](../resources/intune_apps_macosofficesuiteapp.md).|
|[Obtener macOSOfficeSuiteApp](../api/intune_apps_macosofficesuiteapp_get.md)|[macOSOfficeSuiteApp](../resources/intune_apps_macosofficesuiteapp.md)|Lea las propiedades y las relaciones del objeto [macOSOfficeSuiteApp](../resources/intune_apps_macosofficesuiteapp.md).|
|[Crear macOSOfficeSuiteApp](../api/intune_apps_macosofficesuiteapp_create.md)|[macOSOfficeSuiteApp](../resources/intune_apps_macosofficesuiteapp.md)|Cree un objeto [macOSOfficeSuiteApp](../resources/intune_apps_macosofficesuiteapp.md).|
|[Eliminar macOSOfficeSuiteApp](../api/intune_apps_macosofficesuiteapp_delete.md)|Ninguna|Elimina un [macOSOfficeSuiteApp](../resources/intune_apps_macosofficesuiteapp.md).|
|[Actualizar macOSOfficeSuiteApp](../api/intune_apps_macosofficesuiteapp_update.md)|[macOSOfficeSuiteApp](../resources/intune_apps_macosofficesuiteapp.md)|Actualice las propiedades de un objeto [macOSOfficeSuiteApp](../resources/intune_apps_macosofficesuiteapp.md).|

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
  "@odata.type": "microsoft.graph.macOSOfficeSuiteApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.macOSOfficeSuiteApp",
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



