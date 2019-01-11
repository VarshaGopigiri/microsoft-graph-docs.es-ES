---
title: tipo de recurso unaryManagementConditionExpression
description: Una expresión de condición de administración que se evalúa mediante una operación unario.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 619d931e53fbd65419e07ab1b2f27341ccb5dd41
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27829774"
---
# <a name="unarymanagementconditionexpression-resource-type"></a>tipo de recurso unaryManagementConditionExpression

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Una expresión de condición de administración que se evalúa mediante una operación unario.

Hereda de [managementConditionExpressionModel](../resources/intune-fencing-managementconditionexpressionmodel.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Description|
|:---|:---|:---|
|operator|[unaryManagementConditionExpressionOperatorType](../resources/intune-fencing-unarymanagementconditionexpressionoperatortype.md)|El operador utilizado en la evaluación de la operación unario. Los valores posibles son: `not`.|
|operando|[managementConditionExpressionModel](../resources/intune-fencing-managementconditionexpressionmodel.md)|El operando de la operación unario.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.unaryManagementConditionExpression"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.unaryManagementConditionExpression",
  "operator": "String",
  "operand": {
    "@odata.type": "microsoft.graph.managementConditionExpressionModel"
  }
}
```





