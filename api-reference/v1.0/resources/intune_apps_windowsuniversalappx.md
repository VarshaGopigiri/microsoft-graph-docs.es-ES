# <a name="windowsuniversalappx-resource-type"></a>Tipo de recurso windowsUniversalAppX

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades y las propiedades heredadas de la aplicación del conjunto de aplicaciones de línea de negocio de AppX para Windows Universal.

Hereda de [mobileLobApp](../resources/intune_apps_mobilelobapp.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar windowsUniversalAppXs](../api/intune_apps_windowsuniversalappx_list.md)|Colección [windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md)|Enumere las propiedades y las relaciones de los objetos [windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md).|
|[Obtener windowsUniversalAppX](../api/intune_apps_windowsuniversalappx_get.md)|[windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md)|Lea las propiedades y las relaciones del objeto [windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md).|
|[Crear windowsUniversalAppX](../api/intune_apps_windowsuniversalappx_create.md)|[windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md)|Cree un objeto [windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md).|
|[Eliminar windowsUniversalAppX](../api/intune_apps_windowsuniversalappx_delete.md)|Ninguna|Elimina un [windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md).|
|[Actualizar windowsUniversalAppX](../api/intune_apps_windowsuniversalappx_update.md)|[windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md)|Actualice las propiedades de un objeto [windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md).|

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
|committedContentVersion|Cadena|La versión interna confirmada del contenido. Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md)|
|fileName|Cadena|El nombre del archivo de la aplicación de LOB principal. Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md)|
|tamaño|Int64|El tamaño total, incluidos todos los archivos cargados. Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md)|
|applicableArchitectures|Cadena|Las arquitecturas de Windows en las cuales se puede ejecutar esta aplicación. Los valores posibles son: `none`, `x86`, `x64`, `arm` y `neutral`.|
|applicableDeviceTypes|Cadena|Los tipos de dispositivos Windows en los cual se puede ejecutar esta aplicación. Los valores posibles son: `none`, `desktop`, `mobile`, `holographic` y `team`.|
|identityName|Cadena|El nombre de la identidad.|
|identityPublisherHash|Cadena|El hash del publicador de identidad.|
|identityResourceIdentifier|Cadena|El identificador del recurso de identidad.|
|isBundle|Booleano|Si la aplicación es una agrupación o no.|
|minimumSupportedOperatingSystem|[windowsMinimumOperatingSystem](../resources/intune_apps_windowsminimumoperatingsystem.md)|El valor para el sistema operativo mínimo aplicable.|
|identityVersion|Cadena|La versión de identidad.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|categorías|Colección [mobileAppCategory](../resources/intune_apps_mobileappcategory.md)|La lista de categorías para esta aplicación. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|asignaciones|Colección [mobileAppAssignment](../resources/intune_apps_mobileappassignment.md)|La lista de asignaciones de grupo para esta aplicación móvil. Heredado de [mobileApp](../resources/intune_apps_mobileapp.md)|
|contentVersions|Colección [mobileAppContent](../resources/intune_apps_mobileappcontent.md)|La lista de versiones de contenido de esta aplicación. Heredado de [mobileLobApp](../resources/intune_apps_mobilelobapp.md)|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsUniversalAppX"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsUniversalAppX",
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
  "applicableArchitectures": "String",
  "applicableDeviceTypes": "String",
  "identityName": "String",
  "identityPublisherHash": "String",
  "identityResourceIdentifier": "String",
  "isBundle": true,
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.windowsMinimumOperatingSystem",
    "v8_0": true,
    "v8_1": true,
    "v10_0": true
  },
  "identityVersion": "String"
}
```



