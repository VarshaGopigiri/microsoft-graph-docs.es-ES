# <a name="mobileappcategory-resource-type"></a>Tipo de recurso mobileAppCategory

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades de una categoría de aplicación de Intune.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar mobileAppCategories](../api/intune_apps_mobileappcategory_list.md)|Colección [mobileAppCategory](../resources/intune_apps_mobileappcategory.md)|Enumere las propiedades y las relaciones de los objetos [mobileAppCategory](../resources/intune_apps_mobileappcategory.md).|
|[Obtener mobileAppCategory](../api/intune_apps_mobileappcategory_get.md)|[mobileAppCategory](../resources/intune_apps_mobileappcategory.md)|Lea las propiedades y las relaciones del objeto [mobileAppCategory](../resources/intune_apps_mobileappcategory.md).|
|[Crear mobileAppCategory](../api/intune_apps_mobileappcategory_create.md)|[mobileAppCategory](../resources/intune_apps_mobileappcategory.md)|Cree un objeto [mobileAppCategory](../resources/intune_apps_mobileappcategory.md).|
|[Eliminar mobileAppCategory](../api/intune_apps_mobileappcategory_delete.md)|Ninguna|Elimina un [mobileAppCategory](../resources/intune_apps_mobileappcategory.md)|
|[Actualizar mobileAppCategory](../api/intune_apps_mobileappcategory_update.md)|[mobileAppCategory](../resources/intune_apps_mobileappcategory.md)|Actualice las propiedades de un objeto [mobileAppCategory](../resources/intune_apps_mobileappcategory.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|cadena|La clave de la entidad.|
|displayName|cadena|El nombre de la categoría de aplicación.|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora de la última modificación de mobileAppCategory.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.mobileAppCategory"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileAppCategory",
  "id": "String (identifier)",
  "displayName": "String",
  "lastModifiedDateTime": "String (timestamp)"
}
```



