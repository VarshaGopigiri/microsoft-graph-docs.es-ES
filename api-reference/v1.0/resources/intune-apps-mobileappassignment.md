---
title: Tipo de recurso mobileAppAssignment
description: Una clase que contiene las propiedades que se usan para la asignación de grupo de una aplicación móvil.
ms.openlocfilehash: 8fc44919528dd4b5c5ab3d21e082fe2b07aec4e3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030422"
---
# <a name="mobileappassignment-resource-type"></a>Tipo de recurso mobileAppAssignment

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Una clase que contiene las propiedades que se usan para la asignación de grupo de una aplicación móvil.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar mobileAppAssignments](../api/intune-apps-mobileappassignment-list.md)|Colección [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md)|Enumere las propiedades y las relaciones de los objetos [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md).|
|[Obtener mobileAppAssignment](../api/intune-apps-mobileappassignment-get.md)|[mobileAppAssignment](../resources/intune-apps-mobileappassignment.md)|Lea las propiedades y las relaciones del objeto [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md).|
|[Crear mobileAppAssignment](../api/intune-apps-mobileappassignment-create.md)|[mobileAppAssignment](../resources/intune-apps-mobileappassignment.md)|Cree un objeto [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md).|
|[Eliminar mobileAppAssignment](../api/intune-apps-mobileappassignment-delete.md)|Ninguna|Elimina un [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md).|
|[Actualizar mobileAppAssignment](../api/intune-apps-mobileappassignment-update.md)|[mobileAppAssignment](../resources/intune-apps-mobileappassignment.md)|Actualice las propiedades de un objeto [mobileAppAssignment](../resources/intune-apps-mobileappassignment.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad.|
|objetivo|[installIntent](../resources/intune-shared-installintent.md)|El objetivo de instalación definido por el administrador. Los valores posibles son: `available`, `required`, `uninstall` y `availableWithoutEnrollment`.|
|target|[deviceAndAppManagementAssignmentTarget](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|La asignación de grupo de destino definida por el administrador.|
|configuración|[mobileAppAssignmentSettings](../resources/intune-apps-mobileappassignmentsettings.md)|La asignación de la configuración para el destino definida por el administrador.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.mobileAppAssignment"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileAppAssignment",
  "id": "String (identifier)",
  "intent": "String",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  },
  "settings": {
    "@odata.type": "microsoft.graph.mobileAppAssignmentSettings"
  }
}
```



