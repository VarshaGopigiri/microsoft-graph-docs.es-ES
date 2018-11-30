---
title: Tipo de recurso iosVppEBookAssignment
description: Contiene las propiedades que se usan para asignar a un grupo un libro electrónico de VPP para iOS.
ms.openlocfilehash: 88d120963f0762ab04004cd8b90e3fe44d373edd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032446"
---
# <a name="iosvppebookassignment-resource-type"></a>Tipo de recurso iosVppEBookAssignment

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades que se usan para asignar a un grupo un libro electrónico de VPP para iOS.

Hereda de [managedEBookAssignment](../resources/intune-books-managedebookassignment.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar iosVppEBookAssignments](../api/intune-books-iosvppebookassignment-list.md)|Colección [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md)|Enumere las propiedades y las relaciones de los objetos [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md).|
|[Obtener iosVppEBookAssignment](../api/intune-books-iosvppebookassignment-get.md)|[iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md)|Lea las propiedades y las relaciones del objeto [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md).|
|[Crear iosVppEBookAssignment](../api/intune-books-iosvppebookassignment-create.md)|[iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md)|Cree un objeto [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md).|
|[Eliminar iosVppEBookAssignment](../api/intune-books-iosvppebookassignment-delete.md)|Ninguna|Elimina un [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md).|
|[Actualizar iosVppEBookAssignment](../api/intune-books-iosvppebookassignment-update.md)|[iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md)|Actualice las propiedades de un objeto [iosVppEBookAssignment](../resources/intune-books-iosvppebookassignment.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad. Heredado de [managedEBookAssignment](../resources/intune-books-managedebookassignment.md)|
|target|[deviceAndAppManagementAssignmentTarget](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|El destino de la asignación para el libro electrónico. Heredado de [managedEBookAssignment](../resources/intune-books-managedebookassignment.md)|
|installIntent|[installIntent](../resources/intune-shared-installintent.md)|El objetivo de instalación para el libro electrónico. Se hereda de [managedEBookAssignment](../resources/intune-books-managedebookassignment.md). Los valores posibles son: `available`, `required`, `uninstall` y `availableWithoutEnrollment`.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.iosVppEBookAssignment"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosVppEBookAssignment",
  "id": "String (identifier)",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  },
  "installIntent": "String"
}
```



