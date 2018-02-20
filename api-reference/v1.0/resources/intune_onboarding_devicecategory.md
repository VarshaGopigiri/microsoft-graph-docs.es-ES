# <a name="devicecategory-resource-type"></a>Tipo de recurso deviceCategory

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Las categorías de dispositivo proporcionan una forma de organizar sus dispositivos. Al usar categorías de dispositivos, los administradores de la compañía pueden definir las categorías de forma pertinente para su empresa. A continuación, estas categorías se pueden aplicar a un dispositivo en la consola de Azure de Intune o un usuario puede seleccionarlas durante la inscripción de dispositivos. Puede filtrar los informes y crear grupos de dispositivos de Azure Active Directory dinámicos según las categorías de dispositivos.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar deviceCategories](../api/intune_onboarding_devicecategory_list.md)|Colección [deviceCategory](../resources/intune_onboarding_devicecategory.md)|Enumere las propiedades y las relaciones de los objetos [deviceCategory](../resources/intune_onboarding_devicecategory.md).|
|[Obtener deviceCategory](../api/intune_onboarding_devicecategory_get.md)|[deviceCategory](../resources/intune_onboarding_devicecategory.md)|Lea las propiedades y las relaciones del objeto [deviceCategory](../resources/intune_onboarding_devicecategory.md).|
|[Crear deviceCategory](../api/intune_onboarding_devicecategory_create.md)|[deviceCategory](../resources/intune_onboarding_devicecategory.md)|Cree un objeto [deviceCategory](../resources/intune_onboarding_devicecategory.md).|
|[Eliminar deviceCategory](../api/intune_onboarding_devicecategory_delete.md)|Ninguna|Elimina un [deviceCategory](../resources/intune_onboarding_devicecategory.md).|
|[Actualizar deviceCategory](../api/intune_onboarding_devicecategory_update.md)|[deviceCategory](../resources/intune_onboarding_devicecategory.md)|Actualice las propiedades de un objeto [deviceCategory](../resources/intune_onboarding_devicecategory.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|El identificador único de la categoría de dispositivo. Solo lectura.|
|displayName|Cadena|Nombre para mostrar de la categoría de dispositivo.|
|descripción|Cadena|Descripción opcional de la categoría de dispositivo.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceCategory"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceCategory",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String"
}
```



