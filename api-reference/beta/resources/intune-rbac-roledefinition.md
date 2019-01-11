---
title: Tipo de recurso roleDefinition
description: 'El recurso de la definición de rol. La definición de rol es el pilar del acceso basado en roles en Intune. El rol combina un recurso de Intune, como una aplicación móvil, y los permisos de rol asociados para el recurso, como Creación o Lectura. Hay dos tipos de roles: personalizados e integrados. Los roles integrados no se pueden modificar. Tanto los roles personalizados como los integrados deben tener asignaciones que se aplicarán. Cree roles personalizados para definir un rol que permita que se combine cualquier recurso disponible y permiso de rol en un solo rol.'
localization_priority: Normal
ms.openlocfilehash: 27ded12110b7db9e329afc8c90ac114e9296646d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27835675"
---
# <a name="roledefinition-resource-type"></a>Tipo de recurso roleDefinition

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El recurso de la definición de rol. La definición de rol es el pilar del acceso basado en roles en Intune. El rol combina un recurso de Intune, como una aplicación móvil, y los permisos de rol asociados para el recurso, como Creación o Lectura. Hay dos tipos de roles: personalizados e integrados. Los roles integrados no se pueden modificar. Tanto los roles personalizados como los integrados deben tener asignaciones que se aplicarán. Cree roles personalizados para definir un rol que permita que se combine cualquier recurso disponible y permiso de rol en un solo rol.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar roleDefinitions](../api/intune-rbac-roledefinition-list.md)|Colección [roleDefinition](../resources/intune-rbac-roledefinition.md)|Enumere las propiedades y las relaciones de los objetos [roleDefinition](../resources/intune-rbac-roledefinition.md).|
|[Obtener roleDefinition](../api/intune-rbac-roledefinition-get.md)|[roleDefinition](../resources/intune-rbac-roledefinition.md)|Lea las propiedades y las relaciones del objeto [roleDefinition](../resources/intune-rbac-roledefinition.md).|
|[Crear roleDefinition](../api/intune-rbac-roledefinition-create.md)|[roleDefinition](../resources/intune-rbac-roledefinition.md)|Cree un objeto [roleDefinition](../resources/intune-rbac-roledefinition.md).|
|[Eliminar roleDefinition](../api/intune-rbac-roledefinition-delete.md)|Ninguno|Elimina un [roleDefinition](../resources/intune-rbac-roledefinition.md).|
|[Actualizar roleDefinition](../api/intune-rbac-roledefinition-update.md)|[roleDefinition](../resources/intune-rbac-roledefinition.md)|Actualice las propiedades de un objeto [roleDefinition](../resources/intune-rbac-roledefinition.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad. Es de solo lectura y generada automáticamente.|
|displayName|Cadena|Nombre para mostrar de la definición de rol.|
|description|Cadena|Descripción de la definición de rol.|
|permissions|Colección [rolePermission](../resources/intune-rbac-rolepermission.md)|Lista de los permisos de rol que puede realizar este rol. Estos deben coincidir con el actionName que se definió como parte de rolePermission.|
|rolePermissions|Colección [rolePermission](../resources/intune-rbac-rolepermission.md)|Lista de los permisos de rol que puede realizar este rol. Estos deben coincidir con el actionName que se definió como parte de rolePermission.|
|isBuiltInRoleDefinition|Booleano|Tipo de rol. Se establece en True si está integrado o en False si es una definición de rol personalizada.|
|isBuiltIn|Booleano|Tipo de rol. Se establece en True si está integrado o en False si es una definición de rol personalizada.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|roleAssignments|Colección [roleAssignment](../resources/intune-rbac-roleassignment.md)|Lista de asignaciones de rol para este rol.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.roleDefinition"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.roleDefinition",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "permissions": [
    {
      "@odata.type": "microsoft.graph.rolePermission",
      "actions": [
        "String"
      ],
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
  "rolePermissions": [
    {
      "@odata.type": "microsoft.graph.rolePermission",
      "actions": [
        "String"
      ],
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
  "isBuiltInRoleDefinition": true,
  "isBuiltIn": true
}
```





