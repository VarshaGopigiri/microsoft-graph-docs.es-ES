# <a name="deviceandappmanagementroleassignment-resource-type"></a>Tipo de recurso deviceAndAppManagementRoleAssignment

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El recurso de la asignación de roles. Las asignaciones de roles unen la definición de rol con miembros y ámbitos. Puede haber una o más asignaciones de roles por rol. Esto se aplica a los roles integrados y personalizados.

Hereda de [roleAssignment](../resources/intune_rbac_roleassignment.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar deviceAndAppManagementRoleAssignments](../api/intune_rbac_deviceandappmanagementroleassignment_list.md)|Colección [deviceAndAppManagementRoleAssignment](../resources/intune_rbac_deviceandappmanagementroleassignment.md)|Enumere las propiedades y las relaciones de los objetos [deviceAndAppManagementRoleAssignment](../resources/intune_rbac_deviceandappmanagementroleassignment.md).|
|[Obtener deviceAndAppManagementRoleAssignment](../api/intune_rbac_deviceandappmanagementroleassignment_get.md)|[deviceAndAppManagementRoleAssignment](../resources/intune_rbac_deviceandappmanagementroleassignment.md)|Lea las propiedades y las relaciones del objeto [deviceAndAppManagementRoleAssignment](../resources/intune_rbac_deviceandappmanagementroleassignment.md).|
|[Crear deviceAndAppManagementRoleAssignment](../api/intune_rbac_deviceandappmanagementroleassignment_create.md)|[deviceAndAppManagementRoleAssignment](../resources/intune_rbac_deviceandappmanagementroleassignment.md)|Cree un objeto [deviceAndAppManagementRoleAssignment](../resources/intune_rbac_deviceandappmanagementroleassignment.md).|
|[Eliminar deviceAndAppManagementRoleAssignment](../api/intune_rbac_deviceandappmanagementroleassignment_delete.md)|Ninguna|Elimina un [deviceAndAppManagementRoleAssignment](../resources/intune_rbac_deviceandappmanagementroleassignment.md).|
|[Actualizar deviceAndAppManagementRoleAssignment](../api/intune_rbac_deviceandappmanagementroleassignment_update.md)|[deviceAndAppManagementRoleAssignment](../resources/intune_rbac_deviceandappmanagementroleassignment.md)|Actualice las propiedades de un objeto [deviceAndAppManagementRoleAssignment](../resources/intune_rbac_deviceandappmanagementroleassignment.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|cadena|Clave de la entidad. Es de solo lectura y generada automáticamente. Heredado de [roleAssignment](../resources/intune_rbac_roleassignment.md)|
|displayName|cadena|El nombre descriptivo o para mostrar de la asignación de roles. Heredado de [roleAssignment](../resources/intune_rbac_roleassignment.md)|
|descripción|cadena|Descripción de la asignación de roles. Heredado de [roleAssignment](../resources/intune_rbac_roleassignment.md)|
|resourceScopes|Colección de cadenas|Lista de identificadores de grupos de seguridad de miembros del ámbito de roles.  Estos son los identificadores de Azure Active Directory. Heredado de [roleAssignment](../resources/intune_rbac_roleassignment.md)|
|miembros|Colección de cadenas|La lista de identificadores de grupos de seguridad de miembros de roles. Estos son los identificadores de Azure Active Directory.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|roleDefinition|[roleDefinition](../resources/intune_rbac_roledefinition.md)|Definición de rol del que forma parte esta asignación. Heredado de [roleAssignment](../resources/intune_rbac_roleassignment.md)|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceAndAppManagementRoleAssignment"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceAndAppManagementRoleAssignment",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "resourceScopes": [
    "String"
  ],
  "members": [
    "String"
  ]
}
```



