---
title: Tipo de recurso resourceOperation
description: " operación se usa para asignar un recurso de MobileApp a un grupo de seguridad AAD.  No se pueden modificar las operaciones de recursos para los roles integrados."
author: tfitzmac
ms.openlocfilehash: fa004e2f1f41ca03d4b505599ef36e3548c1ab67
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27331468"
---
# <a name="resourceoperation-resource-type"></a>Tipo de recurso resourceOperation

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Define una operación o una acción que puede realizar un recurso (o entidad) de Intune.  Las operaciones comunes son Leer, Eliminar, Actualizar o Crear.  Estas operaciones ofrecen administración básica del propio recurso de Intune subyacente.  En algunos casos, un recurso de Intune puede tener operaciones que el recurso usa para realizar una acción en combinación con otros recursos.  Por ejemplo, la operación de asignación se usa para asignar un recurso MobileApp a un grupo de seguridad de AAD.  No se pueden modificar las operaciones de recursos para los roles integrados. Esto define una acción u operación que se puede realizar en un recurso (o entidad) de Intune.  Las operaciones comunes son Obtener, Enumerar, Actualizar o Crear.  Estas operaciones ofrecen administración básica del propio recurso de Intune subyacente.  En algunos casos, un recurso de Intune puede tener operaciones que el recurso usa para realizar una acción en combinación con otros recursos.  Por ejemplo, la operación "Asignar" se usa para asignar un recurso MobileApp a un grupo de seguridad de AAD.  No se pueden modificar las operaciones de recursos para los roles integrados.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar resourceOperations](../api/intune-rbac-resourceoperation-list.md)|Colección [resourceOperation](../resources/intune-rbac-resourceoperation.md)|Enumere las propiedades y las relaciones de los objetos [resourceOperation](../resources/intune-rbac-resourceoperation.md).|
|[Obtener resourceOperation](../api/intune-rbac-resourceoperation-get.md)|[resourceOperation](../resources/intune-rbac-resourceoperation.md)|Lea las propiedades y las relaciones del objeto [resourceOperation](../resources/intune-rbac-resourceoperation.md).|
|[Crear resourceOperation](../api/intune-rbac-resourceoperation-create.md)|[resourceOperation](../resources/intune-rbac-resourceoperation.md)|Cree un objeto [resourceOperation](../resources/intune-rbac-resourceoperation.md).|
|[Eliminar resourceOperation](../api/intune-rbac-resourceoperation-delete.md)|Ninguno|Elimina un [resourceOperation](../resources/intune-rbac-resourceoperation.md).|
|[Actualizar resourceOperation](../api/intune-rbac-resourceoperation-update.md)|[resourceOperation](../resources/intune-rbac-resourceoperation.md)|Actualice las propiedades de un objeto [resourceOperation](../resources/intune-rbac-resourceoperation.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la operación de recursos. Solo lectura, generada automáticamente.|
|resourceName|String|Nombre del recurso en el que se realiza esta operación.|
|actionName|String|Tipo de acción que va a realizar esta operación. El actionName debe ser conciso y limitado al menor número de palabras posible.|
|description|String|Descripción de la operación de recursos. La descripción se usa en el texto al pasar el mouse para la operación si se muestra en Azure Portal.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.resourceOperation"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.resourceOperation",
  "id": "String (identifier)",
  "resourceName": "String",
  "actionName": "String",
  "description": "String"
}
```



