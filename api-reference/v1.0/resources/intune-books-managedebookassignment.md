---
title: Tipo de recurso managedEBookAssignment
description: Contiene las propiedades que se usan para asignar un libro electrónico a un grupo.
ms.openlocfilehash: ecf79b4055ea87d710cb62ac4446bb5bd65793ee
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031395"
---
# <a name="managedebookassignment-resource-type"></a>Tipo de recurso managedEBookAssignment

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades que se usan para asignar un libro electrónico a un grupo.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar managedEBookAssignments](../api/intune-books-managedebookassignment-list.md)|Colección [managedEBookAssignment](../resources/intune-books-managedebookassignment.md)|Enumere las propiedades y las relaciones de los objetos [managedEBookAssignment](../resources/intune-books-managedebookassignment.md).|
|[Obtener managedEBookAssignment](../api/intune-books-managedebookassignment-get.md)|[managedEBookAssignment](../resources/intune-books-managedebookassignment.md)|Lea las propiedades y las relaciones del objeto [managedEBookAssignment](../resources/intune-books-managedebookassignment.md).|
|[Crear managedEBookAssignment](../api/intune-books-managedebookassignment-create.md)|[managedEBookAssignment](../resources/intune-books-managedebookassignment.md)|Cree un objeto [managedEBookAssignment](../resources/intune-books-managedebookassignment.md).|
|[Eliminar managedEBookAssignment](../api/intune-books-managedebookassignment-delete.md)|Ninguna|Elimina un [managedEBookAssignment](../resources/intune-books-managedebookassignment.md).|
|[Actualizar managedEBookAssignment](../api/intune-books-managedebookassignment-update.md)|[managedEBookAssignment](../resources/intune-books-managedebookassignment.md)|Actualice las propiedades de un objeto [managedEBookAssignment](../resources/intune-books-managedebookassignment.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad.|
|target|[deviceAndAppManagementAssignmentTarget](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|El destino de la asignación para el libro electrónico.|
|installIntent|[installIntent](../resources/intune-shared-installintent.md)|El objetivo de instalación para el libro electrónico. Los valores posibles son: `available`, `required`, `uninstall` y `availableWithoutEnrollment`.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedEBookAssignment"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedEBookAssignment",
  "id": "String (identifier)",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  },
  "installIntent": "String"
}
```



