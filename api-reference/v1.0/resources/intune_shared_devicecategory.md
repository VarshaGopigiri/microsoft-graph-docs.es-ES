# <a name="devicecategory-resource-type"></a>Tipo de recurso deviceCategory

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Las categorías de dispositivo proporcionan una forma de organizar sus dispositivos. Al usar categorías de dispositivos, los administradores de la compañía pueden definir las categorías de forma pertinente para su empresa. A continuación, estas categorías se pueden aplicar a un dispositivo en la consola de Azure de Intune o un usuario puede seleccionarlas durante la inscripción de dispositivos. Puede filtrar los informes y crear grupos de dispositivos de Azure Active Directory dinámicos según las categorías de dispositivos.

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|Objetos [Listar deviceCategories](../api/intune_shared_devicecategory_list.md).|
|Objeto [Obtener deviceCategory](../api/intune_shared_devicecategory_get.md).|
|Objeto [Crear deviceCategory](../api/intune_shared_devicecategory_create.md).|
|[Eliminar deviceCategory](../api/intune_shared_devicecategory_delete.md).|
|Objeto [Actualizar deviceCategory](../api/intune_shared_devicecategory_update.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|El identificador único de la categoría de dispositivo. Solo lectura.|
|**Incorporación**|
|displayName|Cadena|Nombre para mostrar de la categoría de dispositivo.|
|descripción|Cadena|Descripción opcional de la categoría de dispositivo.|

## <a name="relationships"></a>Relaciones
Ninguna

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.deviceCategory"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceCategory",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String"
}
```



