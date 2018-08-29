# <a name="telecomexpensemanagementpartner-resource-type"></a>Tipo de recurso telecomExpenseManagementPartner

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Los recursos telecomExpenseManagementPartner representan los metadatos y el estado de un servicio TEM específico. Una vez que su organización haya incorporado a un partner, este puede estar habilitado o no para activar o desactivar la funcionalidad TEM.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar telecomExpenseManagementPartners](../api/intune_tem_telecomexpensemanagementpartner_list.md)|Colección [telecomExpenseManagementPartner](../resources/intune_tem_telecomexpensemanagementpartner.md)|Enumere las propiedades y las relaciones de los objetos [telecomExpenseManagementPartner](../resources/intune_tem_telecomexpensemanagementpartner.md).|
|[Obtener telecomExpenseManagementPartner](../api/intune_tem_telecomexpensemanagementpartner_get.md)|[telecomExpenseManagementPartner](../resources/intune_tem_telecomexpensemanagementpartner.md)|Lea las propiedades y las relaciones del objeto [telecomExpenseManagementPartner](../resources/intune_tem_telecomexpensemanagementpartner.md).|
|[Crear telecomExpenseManagementPartner](../api/intune_tem_telecomexpensemanagementpartner_create.md)|[telecomExpenseManagementPartner](../resources/intune_tem_telecomexpensemanagementpartner.md)|Cree un objeto [telecomExpenseManagementPartner](../resources/intune_tem_telecomexpensemanagementpartner.md).|
|[Eliminar telecomExpenseManagementPartner](../api/intune_tem_telecomexpensemanagementpartner_delete.md)|Ninguna|Elimina un [telecomExpenseManagementPartner](../resources/intune_tem_telecomexpensemanagementpartner.md).|
|[Actualizar telecomExpenseManagementPartner](../api/intune_tem_telecomexpensemanagementpartner_update.md)|[telecomExpenseManagementPartner](../resources/intune_tem_telecomexpensemanagementpartner.md)|Actualice las propiedades de un objeto [telecomExpenseManagementPartner](../resources/intune_tem_telecomexpensemanagementpartner.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Identificador único del partner de TEM.|
|displayName|String|Nombre para mostrar del partner de TEM.|
|url|String|Dirección URL del panel de control administrativo del partner de TEM, donde un administrador puede configurar el servicio de su TEM.|
|appAuthorized|Boolean|Si se ha autorizado a la aplicación de AAD del partner para que obtenga acceso a Intune.|
|enabled|Boolean|Si la conexión de Intune al servicio de TEM está habilitada o deshabilitada.|
|lastConnectionDateTime|DateTimeOffset|Marca de tiempo de la última solicitud enviada a Intune por el partner de TEM.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.telecomExpenseManagementPartner"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.telecomExpenseManagementPartner",
  "id": "String (identifier)",
  "displayName": "String",
  "url": "String",
  "appAuthorized": true,
  "enabled": true,
  "lastConnectionDateTime": "String (timestamp)"
}
```



