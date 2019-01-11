---
title: Tipo de recurso mobileAppAssignment
description: Una clase que contiene las propiedades que se usan para la asignación de grupo de una aplicación móvil.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 3eefc11d0e0df41ea452d903bcc159a2fbe2865e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27839515"
---
# <a name="mobileappassignment-resource-type"></a>Tipo de recurso mobileAppAssignment

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

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
|id|Cadena|Clave de la entidad.|
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





