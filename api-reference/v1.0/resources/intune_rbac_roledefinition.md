# <a name="roledefinition-resource-type"></a>Tipo de recurso roleDefinition

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El recurso de la definición de rol. La definición de rol es el pilar del acceso basado en roles en Intune. El rol combina un recurso de Intune, como una aplicación móvil, y los permisos de rol asociados para el recurso, como Creación o Lectura. Hay dos tipos de roles: personalizados e integrados. Los roles integrados no se pueden modificar. Tanto los roles personalizados como los integrados deben tener asignaciones que se aplicarán. Cree roles personalizados para definir un rol que permita que se combine cualquier recurso disponible y permiso de rol en un solo rol.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar roleDefinitions](../api/intune_rbac_roledefinition_list.md)|Colección [roleDefinition](../resources/intune_rbac_roledefinition.md)|Enumere las propiedades y las relaciones de los objetos [roleDefinition](../resources/intune_rbac_roledefinition.md).|
|[Obtener roleDefinition](../api/intune_rbac_roledefinition_get.md)|[roleDefinition](../resources/intune_rbac_roledefinition.md)|Lea las propiedades y las relaciones del objeto [roleDefinition](../resources/intune_rbac_roledefinition.md).|
|[Crear roleDefinition](../api/intune_rbac_roledefinition_create.md)|[roleDefinition](../resources/intune_rbac_roledefinition.md)|Cree un objeto [roleDefinition](../resources/intune_rbac_roledefinition.md).|
|[Eliminar roleDefinition](../api/intune_rbac_roledefinition_delete.md)|Ninguno|Elimina un [roleDefinition](../resources/intune_rbac_roledefinition.md).|
|[Actualizar roleDefinition](../api/intune_rbac_roledefinition_update.md)|[roleDefinition](../resources/intune_rbac_roledefinition.md)|Actualice las propiedades de un objeto [roleDefinition](../resources/intune_rbac_roledefinition.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad. Es de solo lectura y generada automáticamente.|
|displayName|String|Nombre para mostrar de la definición de rol.|
|description|String|Descripción de la definición de rol.|
|rolePermissions|Colección [rolePermission](../resources/intune_rbac_rolepermission.md)|Lista de los permisos de rol que puede realizar este rol. Estos deben coincidir con el actionName que se definió como parte de rolePermission.|
|isBuiltIn|Boolean|Tipo de rol. Se establece en True si está integrado o en False si es una definición de rol personalizada.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|roleAssignments|Colección [roleAssignment](../resources/intune_rbac_roleassignment.md)|Lista de asignaciones de rol para este rol.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.roleDefinition"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.roleDefinition",
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



