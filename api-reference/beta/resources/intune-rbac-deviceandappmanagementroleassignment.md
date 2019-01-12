---
title: Tipo de recurso deviceAndAppManagementRoleAssignment
description: El recurso de la asignación de roles. Las asignaciones de roles unen la definición de rol con miembros y ámbitos. Puede haber una o más asignaciones de roles por rol. Esto se aplica a los roles integrados y personalizados.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 5ad9df8713a0238a7d09b92acc525f3822636c96
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27985189"
---
# <a name="deviceandappmanagementroleassignment-resource-type"></a>Tipo de recurso deviceAndAppManagementRoleAssignment

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El recurso de la asignación de roles. Las asignaciones de roles unen la definición de rol con miembros y ámbitos. Puede haber una o más asignaciones de roles por rol. Esto se aplica a los roles integrados y personalizados.

Hereda de [roleAssignment](../resources/intune-rbac-roleassignment.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar deviceAndAppManagementRoleAssignments](../api/intune-rbac-deviceandappmanagementroleassignment-list.md)|Colección [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md)|Enumere las propiedades y las relaciones de los objetos [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md).|
|[Obtener deviceAndAppManagementRoleAssignment](../api/intune-rbac-deviceandappmanagementroleassignment-get.md)|[deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md)|Lea las propiedades y las relaciones del objeto [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md).|
|[Crear deviceAndAppManagementRoleAssignment](../api/intune-rbac-deviceandappmanagementroleassignment-create.md)|[deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md)|Cree un objeto [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md).|
|[Eliminar deviceAndAppManagementRoleAssignment](../api/intune-rbac-deviceandappmanagementroleassignment-delete.md)|Ninguna|Elimina un [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md).|
|[Actualizar deviceAndAppManagementRoleAssignment](../api/intune-rbac-deviceandappmanagementroleassignment-update.md)|[deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md)|Actualice las propiedades de un objeto [deviceAndAppManagementRoleAssignment](../resources/intune-rbac-deviceandappmanagementroleassignment.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad. Es de solo lectura y generada automáticamente. Heredado de [roleAssignment](../resources/intune-rbac-roleassignment.md)|
|displayName|Cadena|El nombre descriptivo o para mostrar de la asignación de roles. Heredado de [roleAssignment](../resources/intune-rbac-roleassignment.md)|
|descripción|Cadena|Descripción de la asignación de roles. Heredado de [roleAssignment](../resources/intune-rbac-roleassignment.md)|
|scopeMembers|Colección string|Lista de identificadores de grupos de seguridad de miembros del ámbito de roles.  Estos son los identificadores de Azure Active Directory. Heredado de [roleAssignment](../resources/intune-rbac-roleassignment.md)|
|scopeType|[roleAssignmentScopeType](../resources/intune-rbac-roleassignmentscopetype.md)|Especifica el tipo de ámbito para una asignación de roles. El tipo predeterminado 'ResourceScope' permite la asignación de ResourceScopes. Para 'AllDevices', 'AllLicensedUsers' y 'AllDevicesAndLicensedUsers', la propiedad ResourceScopes debería dejarse vacía. Se hereda de [roleAssignment](../resources/intune-rbac-roleassignment.md). Los valores posibles son: `resourceScope`, `allDevices`, `allLicensedUsers` y `allDevicesAndLicensedUsers`.|
|resourceScopes|Colección string|Lista de identificadores de grupos de seguridad de miembros del ámbito de roles.  Estos son los identificadores de Azure Active Directory. Heredado de [roleAssignment](../resources/intune-rbac-roleassignment.md)|
|members|Colección string|La lista de identificadores de grupos de seguridad de miembros de roles. Estos son los identificadores de Azure Active Directory.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|roleDefinition|[roleDefinition](../resources/intune-rbac-roledefinition.md)|Definición de rol del que forma parte esta asignación. Heredado de [roleAssignment](../resources/intune-rbac-roleassignment.md)|
|roleScopeTags|colección de [roleScopeTag](../resources/intune-rbac-rolescopetag.md)|El conjunto de etiquetas de ámbito de función definida en la asignación de roles.|

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
  "scopeMembers": [
    "String"
  ],
  "scopeType": "String",
  "resourceScopes": [
    "String"
  ],
  "members": [
    "String"
  ]
}
```





