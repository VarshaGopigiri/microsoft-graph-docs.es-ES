---
title: Tipo de recurso resourceOperation
description: " operación se usa para asignar un recurso de MobileApp a un grupo de seguridad AAD.  No se pueden modificar las operaciones de recursos para los roles integrados."
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: fd8a0620c56299446d8c0315ca66b318c7e6d71c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27914790"
---
# <a name="resourceoperation-resource-type"></a>Tipo de recurso resourceOperation

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

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
|[getScopesForUser (función)](../api/intune-rbac-resourceoperation-getscopesforuser.md)|Colección de cadenas|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la operación de recursos. Solo lectura, generada automáticamente.|
|resource|String|Categoría de recurso al que pertenece esta operación.|
|resourceName|String|Nombre del recurso en el que se realiza esta operación.|
|actionName|Cadena|Tipo de acción que va a realizar esta operación. El actionName debe ser conciso y limitado al menor número de palabras posible.|
|description|String|Descripción de la operación de recursos. La descripción se usa en el texto al pasar el mouse para la operación si se muestra en Azure Portal.|
|enabledForScopeValidation|Booleano|Determina si el permiso se valida para ámbitos definidos por la asignación de roles.|

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
  "resource": "String",
  "resourceName": "String",
  "actionName": "String",
  "description": "String",
  "enabledForScopeValidation": true
}
```





