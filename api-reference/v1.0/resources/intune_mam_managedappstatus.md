# <a name="managedappstatus-resource-type"></a>Tipo de recurso managedAppStatus

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Representa el estado de protección y configuración de la aplicación para la organización.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar managedAppStatuses](../api/intune_mam_managedappstatus_list.md)|Colección [managedAppStatus](../resources/intune_mam_managedappstatus.md)|Enumere las propiedades y las relaciones de los objetos [managedAppStatus](../resources/intune_mam_managedappstatus.md).|
|[Obtener managedAppStatus](../api/intune_mam_managedappstatus_get.md)|[managedAppStatus](../resources/intune_mam_managedappstatus.md)|Lea las propiedades y las relaciones del objeto [managedAppStatus](../resources/intune_mam_managedappstatus.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|displayName|String|Nombre descriptivo del informe de estado.|
|id|Cadena|Clave de la entidad.|
|version|String|Versión de la entidad.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "abstract": true,
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.managedAppStatus"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAppStatus",
  "displayName": "String",
  "id": "String (identifier)",
  "version": "String"
}
```



