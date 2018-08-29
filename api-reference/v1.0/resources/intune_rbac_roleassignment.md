# <a name="roleassignment-resource-type"></a>Tipo de recurso roleAssignment

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El recurso de la asignación de roles. Las asignaciones de roles unen la definición de rol con miembros y ámbitos. Puede haber una o más asignaciones de roles por rol. Esto se aplica a los roles integrados y personalizados.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar roleAssignments](../api/intune_rbac_roleassignment_list.md)|Colección [roleAssignment](../resources/intune_rbac_roleassignment.md)|Enumere las propiedades y las relaciones de los objetos [roleAssignment](../resources/intune_rbac_roleassignment.md).|
|[Obtener roleAssignment](../api/intune_rbac_roleassignment_get.md)|[roleAssignment](../resources/intune_rbac_roleassignment.md)|Lea las propiedades y las relaciones del objeto [roleAssignment](../resources/intune_rbac_roleassignment.md).|
|[Crear roleAssignment](../api/intune_rbac_roleassignment_create.md)|[roleAssignment](../resources/intune_rbac_roleassignment.md)|Cree un objeto [roleAssignment](../resources/intune_rbac_roleassignment.md).|
|[Eliminar roleAssignment](../api/intune_rbac_roleassignment_delete.md)|Ninguna|Elimina un [roleAssignment](../resources/intune_rbac_roleassignment.md).|
|[Actualizar roleAssignment](../api/intune_rbac_roleassignment_update.md)|[roleAssignment](../resources/intune_rbac_roleassignment.md)|Actualice las propiedades de un objeto [roleAssignment](../resources/intune_rbac_roleassignment.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad. Es de solo lectura y generada automáticamente.|
|displayName|String|El nombre descriptivo o para mostrar de la asignación de roles.|
|descripción|String|Descripción de la asignación de roles.|
|resourceScopes|Colección string|Lista de identificadores de grupos de seguridad de miembros del ámbito de roles.  Estos son los identificadores de Azure Active Directory.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|roleDefinition|[roleDefinition](../resources/intune_rbac_roledefinition.md)|Definición de rol del que forma parte esta asignación.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.roleAssignment"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.roleAssignment",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "resourceScopes": [
    "String"
  ]
}
```



