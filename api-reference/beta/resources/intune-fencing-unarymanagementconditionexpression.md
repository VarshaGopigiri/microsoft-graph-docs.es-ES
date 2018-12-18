---
title: tipo de recurso unaryManagementConditionExpression
description: Una expresión de condición de administración que se evalúa mediante una operación unario.
author: tfitzmac
ms.openlocfilehash: 43711e68d88bdf0854e8501377fbf3e30b25b3ec
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27344348"
---
# <a name="unarymanagementconditionexpression-resource-type"></a>tipo de recurso unaryManagementConditionExpression

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Una expresión de condición de administración que se evalúa mediante una operación unario.

Hereda de [managementConditionExpressionModel](../resources/intune-fencing-managementconditionexpressionmodel.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
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





