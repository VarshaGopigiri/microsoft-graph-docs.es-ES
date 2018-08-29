# <a name="managedappoperation-resource-type"></a>Tipo de recurso managedAppOperation

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Representa una operación que se aplica a un registro de la aplicación.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar managedAppOperations](../api/intune_mam_managedappoperation_list.md)|Colección [managedAppOperation](../resources/intune_mam_managedappoperation.md)|Enumere las propiedades y las relaciones de los objetos [managedAppOperation](../resources/intune_mam_managedappoperation.md).|
|[Obtener managedAppOperation](../api/intune_mam_managedappoperation_get.md)|[managedAppOperation](../resources/intune_mam_managedappoperation.md)|Lea las propiedades y las relaciones del objeto [managedAppOperation](../resources/intune_mam_managedappoperation.md).|
|[Crear managedAppOperation](../api/intune_mam_managedappoperation_create.md)|[managedAppOperation](../resources/intune_mam_managedappoperation.md)|Cree un objeto [managedAppOperation](../resources/intune_mam_managedappoperation.md).|
|[Eliminar managedAppOperation](../api/intune_mam_managedappoperation_delete.md)|Ninguna|Elimina un [managedAppOperation](../resources/intune_mam_managedappoperation.md).|
|[Actualizar managedAppOperation](../api/intune_mam_managedappoperation_update.md)|[managedAppOperation](../resources/intune_mam_managedappoperation.md)|Actualice las propiedades de un objeto [managedAppOperation](../resources/intune_mam_managedappoperation.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|displayName|String|El nombre de la operación.|
|lastModifiedDateTime|DateTimeOffset|La última vez que se modificó el funcionamiento de la aplicación.|
|estado|String|El estado actual de la operación|
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
  "@odata.type": "microsoft.graph.managedAppOperation"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAppOperation",
  "displayName": "String",
  "lastModifiedDateTime": "String (timestamp)",
  "state": "String",
  "id": "String (identifier)",
  "version": "String"
}
```



