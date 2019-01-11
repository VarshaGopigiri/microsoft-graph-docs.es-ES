---
title: Tipo de recurso deviceAndAppManagementRoleDefinition
description: 'El recurso de la definición de rol. La definición de rol es el pilar del acceso basado en roles en Intune. El rol combina un recurso de Intune, como una aplicación móvil, y los permisos de rol asociados para el recurso, como Creación o Lectura. Hay dos tipos de roles: personalizados e integrados. Los roles integrados no se pueden modificar. Tanto los roles personalizados como los integrados deben tener asignaciones que se aplicarán. Cree roles personalizados para definir un rol que permita que se combine cualquier recurso disponible y permiso de rol en un solo rol.'
localization_priority: Normal
ms.openlocfilehash: a7bdf06be22c2efb11e7fbccf2bd76e5bb9459a5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27805260"
---
# <a name="deviceandappmanagementroledefinition-resource-type"></a>Tipo de recurso deviceAndAppManagementRoleDefinition

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El recurso de la definición de rol. La definición de rol es el pilar del acceso basado en roles en Intune. El rol combina un recurso de Intune, como una aplicación móvil, y los permisos de rol asociados para el recurso, como Creación o Lectura. Hay dos tipos de roles: personalizados e integrados. Los roles integrados no se pueden modificar. Tanto los roles personalizados como los integrados deben tener asignaciones que se aplicarán. Cree roles personalizados para definir un rol que permita que se combine cualquier recurso disponible y permiso de rol en un solo rol.

Hereda de [roleDefinition](../resources/intune-rbac-roledefinition.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar deviceAndAppManagementRoleDefinitions](../api/intune-rbac-deviceandappmanagementroledefinition-list.md)|Colección [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md)|Enumere las propiedades y las relaciones de los objetos [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md).|
|[Obtener deviceAndAppManagementRoleDefinition](../api/intune-rbac-deviceandappmanagementroledefinition-get.md)|[deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md)|Lea las propiedades y las relaciones del objeto [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md).|
|[Crear deviceAndAppManagementRoleDefinition](../api/intune-rbac-deviceandappmanagementroledefinition-create.md)|[deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md)|Cree un objeto [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md).|
|[Eliminar deviceAndAppManagementRoleDefinition](../api/intune-rbac-deviceandappmanagementroledefinition-delete.md)|Ninguna|Elimina un[deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md).|
|[Actualizar deviceAndAppManagementRoleDefinition](../api/intune-rbac-deviceandappmanagementroledefinition-update.md)|[deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md)|Actualice las propiedades de un objeto [deviceAndAppManagementRoleDefinition](../resources/intune-rbac-deviceandappmanagementroledefinition.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad. Es de solo lectura y generada automáticamente. Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)|
|displayName|Cadena|Nombre para mostrar de la definición de rol. Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)|
|descripción|Cadena|Descripción de la definición de rol. Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)|
|permissions|Colección [rolePermission](../resources/intune-rbac-rolepermission.md)|Lista de los permisos de rol que puede realizar este rol. Estos deben coincidir con el actionName que se definió como parte de rolePermission. Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)|
|rolePermissions|Colección [rolePermission](../resources/intune-rbac-rolepermission.md)|Lista de los permisos de rol que puede realizar este rol. Estos deben coincidir con el actionName que se definió como parte de rolePermission. Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)|
|isBuiltInRoleDefinition|Booleano|Tipo de rol. Se establece en True si está integrado o en False si es una definición de rol personalizada. Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)|
|isBuiltIn|Booleano|Tipo de rol. Se establece en True si está integrado o en False si es una definición de rol personalizada. Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|roleAssignments|Colección [roleAssignment](../resources/intune-rbac-roleassignment.md)|Lista de asignaciones de rol para este rol. Heredado de [roleDefinition](../resources/intune-rbac-roledefinition.md)|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceAndAppManagementRoleDefinition"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceAndAppManagementRoleDefinition",
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





