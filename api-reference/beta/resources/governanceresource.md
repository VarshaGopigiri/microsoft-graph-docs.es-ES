---
title: tipo de recurso governanceResource
description: Representa los recursos que se pueden administrar mediante la administración de identidad con privilegios (PIM). Para obtener recursos de Azure, puede ser una suscripción a un grupo de recursos y un recurso, como una máquina virtual, una base de datos de SQL, etcetera.
ms.openlocfilehash: 9e47f1295f9498796d51414a0a97acbe51fe1aae
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087423"
---
# <a name="governanceresource-resource-type"></a>tipo de recurso governanceResource

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa los recursos que se pueden administrar mediante la administración de identidad con privilegios (PIM). Para obtener recursos de Azure, puede ser una suscripción a un grupo de recursos y un recurso, como una máquina virtual, una base de datos de SQL, etcetera.


## <a name="methods"></a>Métodos

| Método          | Tipo de valor devuelto |Descripción|
|:---------------|:--------|:----------|
|[List](../api/governanceresource-list.md) | colección de [governanceResource](../resources/governanceresource.md)|Una colección de recursos que el solicitante tiene acceso a los de la lista.|
|[Get](../api/governanceresource-get.md) | [governanceResource](../resources/governanceresource.md) |Propiedades de lectura y las relaciones de una entidad de recurso especificado por id.|

No `POST`, `PUT`, `PATCH`, `DELETE` son compatibles con `roleDefinitions` conjunto de entidades por ahora.

## <a name="properties"></a>Propiedades
| Propiedad          |Tipo         |Descripción|
|:------------------|:----------|:----------|
|id                 |String     |El identificador del recurso. Está en formato de GUID.|
|externalId           |String   |El identificador externo del recurso, que representa su identificador original en la base de datos externo. Por ejemplo, el identificador de un recurso de suscripción externo puede ser "/ suscripciones/c14ae696-5e0c-4e5d-88cc-bef6637737ac". |
|type               |Cadena     |Necesario. Tipo de recurso. Por ejemplo, para los recursos de Azure, el tipo podría ser "Suscripción", "ResourceGroup", "Microsoft.Sql/server", etcetera.|
|displayName        |String     |El nombre para mostrar del recurso.|
|status             |String     |El estado de un recurso determinado. Por ejemplo, podría representar si el recurso está bloqueado o no (valores: `Active` / `Locked`). Nota: Esta propiedad puede ampliarse en el futuro para admitir escenarios más.|
|onboardDateTime|DateTimeOffset      |Representa la fecha hora cuando se inicia el recurso administrado por PIM.|
|roleAssignmentCount|Int32      |Opcional. El número de asignaciones de roles para el recurso determinado. Para obtener la propiedad, por favor, use explícitamente `$select=roleAssignmentCount` en la consulta.|
|roleDefinitionCount|Int32      |Opcional. El número de definiciones de roles para el recurso determinado. Para obtener la propiedad, por favor, use explícitamente `$select=roleDefinitionCount` en la consulta.|
|permissions|[governancePermission](../resources/governancepermission.md)      |Opcional. Representa el estado de acceso del solicitante para el recurso. Para obtener la propiedad, por favor, use explícitamente `$select=permissions` en la consulta.|

## <a name="relationships"></a>Relaciones
| Relación   | Tipo                                         |Descripción|
|:---------------|:---------------------------------------------|:----------|
|roleAssignments |colección de [governanceRoleAssignment](../resources/governanceroleassignment.md)|La colección de asignaciones de roles para el recurso.|
|roleDefinitions |colección de [governanceRoleDefinition](../resources/governanceroledefinition.md)|La colección de definiciones de rol para el recurso.|
|roleAssignmentRequests |colección de [governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md)|La colección de solicitudes de asignación de rol para el recurso.|
|roleSettings |colección de [governanceRoleSetting](../resources/governancerolesetting.md)|La colección de configuración de las funciones para el recurso.|
|primario          |[governanceResource](../resources/governanceresource.md)           |Solo lectura. El recurso primario. para `pimforazurerbac` escenario, puede representar la suscripción a la que pertenece el recurso.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.governanceResource"
}-->
```json
{
  "id": "String (identifier)",
  "externalId": "String",
  "type": "String",
  "displayName": "String",
  "status": "String"
}

```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "governanceResource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->