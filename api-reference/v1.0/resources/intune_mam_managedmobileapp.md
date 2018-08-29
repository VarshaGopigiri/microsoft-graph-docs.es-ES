# <a name="managedmobileapp-resource-type"></a>Tipo de recurso managedMobileApp

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El identificador de la implementación de una aplicación.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar managedMobileApps](../api/intune_mam_managedmobileapp_list.md)|Colección [managedMobileApp](../resources/intune_mam_managedmobileapp.md)|Enumere las propiedades y las relaciones de los objetos [managedMobileApp](../resources/intune_mam_managedmobileapp.md).|
|[Obtener managedMobileApp](../api/intune_mam_managedmobileapp_get.md)|[managedMobileApp](../resources/intune_mam_managedmobileapp.md)|Lea las propiedades y las relaciones del objeto [managedMobileApp](../resources/intune_mam_managedmobileapp.md).|
|[Crear managedMobileApp](../api/intune_mam_managedmobileapp_create.md)|[managedMobileApp](../resources/intune_mam_managedmobileapp.md)|Cree un objeto [managedMobileApp](../resources/intune_mam_managedmobileapp.md).|
|[Eliminar managedMobileApp](../api/intune_mam_managedmobileapp_delete.md)|Ninguna|Elimina un [managedMobileApp](../resources/intune_mam_managedmobileapp.md).|
|[Actualizar managedMobileApp](../api/intune_mam_managedmobileapp_update.md)|[managedMobileApp](../resources/intune_mam_managedmobileapp.md)|Actualice las propiedades de un objeto [managedMobileApp](../resources/intune_mam_managedmobileapp.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|mobileAppIdentifier|[mobileAppIdentifier](../resources/intune_mam_mobileappidentifier.md)|El identificador de una aplicación con el tipo de sistema operativo.|
|id|Cadena|Clave de la entidad.|
|version|String|Versión de la entidad.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.managedMobileApp"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.managedMobileApp",
  "mobileAppIdentifier": {
    "@odata.type": "microsoft.graph.mobileAppIdentifier"
  },
  "id": "String (identifier)",
  "version": "String"
}
```



