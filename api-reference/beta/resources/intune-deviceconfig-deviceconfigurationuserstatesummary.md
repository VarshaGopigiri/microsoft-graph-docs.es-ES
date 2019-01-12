---
title: tipo de recurso deviceConfigurationUserStateSummary
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: d5c1a6f20a54f74d077adf26de81812fe9ed5fee
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27943770"
---
# <a name="deviceconfigurationuserstatesummary-resource-type"></a>tipo de recurso deviceConfigurationUserStateSummary

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener deviceConfigurationUserStateSummary](../api/intune-deviceconfig-deviceconfigurationuserstatesummary-get.md)|[deviceConfigurationUserStateSummary](../resources/intune-deviceconfig-deviceconfigurationuserstatesummary.md)|Leer las propiedades y las relaciones del objeto [deviceConfigurationUserStateSummary](../resources/intune-deviceconfig-deviceconfigurationuserstatesummary.md) .|
|[Actualizar deviceConfigurationUserStateSummary](../api/intune-deviceconfig-deviceconfigurationuserstatesummary-update.md)|[deviceConfigurationUserStateSummary](../resources/intune-deviceconfig-deviceconfigurationuserstatesummary.md)|Actualizar las propiedades de un objeto [deviceConfigurationUserStateSummary](../resources/intune-deviceconfig-deviceconfigurationuserstatesummary.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad.|
|unknownUserCount|Int32|Número de usuarios desconocidos|
|notApplicableUserCount|Int32|Número de usuarios no es aplicable.|
|compliantUserCount|Int32|Número de usuarios compatible con|
|remediatedUserCount|Int32|Número de usuarios corregidos con pruebas|
|nonCompliantUserCount|Int32|Número de usuarios no compatibles|
|errorUserCount|Int32|Número de usuarios de error|
|conflictUserCount|Int32|Número de usuarios de conflicto|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceConfigurationUserStateSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceConfigurationUserStateSummary",
  "id": "String (identifier)",
  "unknownUserCount": 1024,
  "notApplicableUserCount": 1024,
  "compliantUserCount": 1024,
  "remediatedUserCount": 1024,
  "nonCompliantUserCount": 1024,
  "errorUserCount": 1024,
  "conflictUserCount": 1024
}
```





