# <a name="deviceandappmanagementroledefinition-resource-type"></a>Tipo de recurso deviceAndAppManagementRoleDefinition

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El recurso de la definición de rol. La definición de rol es el pilar del acceso basado en roles en Intune. El rol combina un recurso de Intune, como una aplicación móvil, y los permisos de rol asociados para el recurso, como Creación o Lectura. Hay dos tipos de roles: personalizados e integrados. Los roles integrados no se pueden modificar. Tanto los roles personalizados como los integrados deben tener asignaciones que se aplicarán. Cree roles personalizados para definir un rol que permita que se combine cualquier recurso disponible y permiso de rol en un solo rol.

Hereda de [roleDefinition](../resources/intune_rbac_roledefinition.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar deviceAndAppManagementRoleDefinitions](../api/intune_rbac_deviceandappmanagementroledefinition_list.md)|Colección [deviceAndAppManagementRoleDefinition](../resources/intune_rbac_deviceandappmanagementroledefinition.md)|Enumere las propiedades y las relaciones de los objetos [deviceAndAppManagementRoleDefinition](../resources/intune_rbac_deviceandappmanagementroledefinition.md).|
|[Obtener deviceAndAppManagementRoleDefinition](../api/intune_rbac_deviceandappmanagementroledefinition_get.md)|[deviceAndAppManagementRoleDefinition](../resources/intune_rbac_deviceandappmanagementroledefinition.md)|Lea las propiedades y las relaciones del objeto [deviceAndAppManagementRoleDefinition](../resources/intune_rbac_deviceandappmanagementroledefinition.md).|
|[Crear deviceAndAppManagementRoleDefinition](../api/intune_rbac_deviceandappmanagementroledefinition_create.md)|[deviceAndAppManagementRoleDefinition](../resources/intune_rbac_deviceandappmanagementroledefinition.md)|Cree un objeto [deviceAndAppManagementRoleDefinition](../resources/intune_rbac_deviceandappmanagementroledefinition.md).|
|[Eliminar deviceAndAppManagementRoleDefinition](../api/intune_rbac_deviceandappmanagementroledefinition_delete.md)|Ninguna|Elimina un[deviceAndAppManagementRoleDefinition](../resources/intune_rbac_deviceandappmanagementroledefinition.md).|
|[Actualizar deviceAndAppManagementRoleDefinition](../api/intune_rbac_deviceandappmanagementroledefinition_update.md)|[deviceAndAppManagementRoleDefinition](../resources/intune_rbac_deviceandappmanagementroledefinition.md)|Actualice las propiedades de un objeto [deviceAndAppManagementRoleDefinition](../resources/intune_rbac_deviceandappmanagementroledefinition.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad. Es de solo lectura y generada automáticamente. Heredado de [roleDefinition](../resources/intune_rbac_roledefinition.md)|
|displayName|String|Nombre para mostrar de la definición de rol. Heredado de [roleDefinition](../resources/intune_rbac_roledefinition.md)|
|descripción|String|Descripción de la definición de rol. Heredado de [roleDefinition](../resources/intune_rbac_roledefinition.md)|
|rolePermissions|Colección [rolePermission](../resources/intune_rbac_rolepermission.md)|Lista de los permisos de rol que puede realizar este rol. Estos deben coincidir con el actionName que se definió como parte de rolePermission. Heredado de [roleDefinition](../resources/intune_rbac_roledefinition.md)|
|isBuiltIn|Boolean|Tipo de rol. Se establece en True si está integrado o en False si es una definición de rol personalizada. Heredado de [roleDefinition](../resources/intune_rbac_roledefinition.md)|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|roleAssignments|Colección [roleAssignment](../resources/intune_rbac_roleassignment.md)|Lista de asignaciones de rol para este rol. Heredado de [roleDefinition](../resources/intune_rbac_roledefinition.md)|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "keyProperty": "id",
  "baseType": "microsoft.graph.roleDefinition",
  "@odata.type": "microsoft.graph.deviceAndAppManagementRoleDefinition"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceAndAppManagementRoleDefinition",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "rolePermissions": [
    {
      "@odata.type": "microsoft.graph.rolePermission",
      "resourceActions": [
        {
          "@odata.type": "microsoft.graph.resourceAction",
          "allowedResourceActions": [
            "String"
          ],
          "notAllowedResourceActions": [
            "String"
          ]
        }
      ]
    }
  ],
  "isBuiltIn": true
}
```



