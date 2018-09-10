# <a name="mobileappcontent-resource-type"></a>Tipo de recurso mobileAppContent

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades del contenido de una versión de aplicación específica. Cada mobileAppContent puede tener varios mobileAppContentFile.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar mobileAppContents](../api/intune_apps_mobileappcontent_list.md)|Colección [mobileAppContent](../resources/intune_apps_mobileappcontent.md)|Enumere las propiedades y las relaciones de los objetos [mobileAppContent](../resources/intune_apps_mobileappcontent.md).|
|[Obtener mobileAppContent](../api/intune_apps_mobileappcontent_get.md)|[mobileAppContent](../resources/intune_apps_mobileappcontent.md)|Lea las propiedades y las relaciones del objeto [mobileAppContent](../resources/intune_apps_mobileappcontent.md).|
|[Crear mobileAppContent](../api/intune_apps_mobileappcontent_create.md)|[mobileAppContent](../resources/intune_apps_mobileappcontent.md)|Cree un objeto [mobileAppContent](../resources/intune_apps_mobileappcontent.md).|
|[Eliminar mobileAppContent](../api/intune_apps_mobileappcontent_delete.md)|Ninguna|Elimina un [mobileAppContent](../resources/intune_apps_mobileappcontent.md)|
|[Actualizar mobileAppContent](../api/intune_apps_mobileappcontent_update.md)|[mobileAppContent](../resources/intune_apps_mobileappcontent.md)|Actualice las propiedades de un objeto [mobileAppContent](../resources/intune_apps_mobileappcontent.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|La versión de contenido de la aplicación.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|archivos|Colección [mobileAppContentFile](../resources/intune_apps_mobileappcontentfile.md)|La lista de archivos de esta versión de contenido de la aplicación.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.mobileAppContent"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileAppContent",
  "id": "String (identifier)"
}
```








