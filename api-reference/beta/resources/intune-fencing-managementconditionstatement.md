---
title: tipo de recurso managementConditionStatement
description: Una instrucción de condición de administración es un grupo de condiciones de administración que habilitar o deshabilitar las configuraciones de dispositivo o la aplicación cuando se cumplen todas las condiciones de administración contenido.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: c6281d151555c0c58a0eb608e9dafc754384369f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27878403"
---
# <a name="managementconditionstatement-resource-type"></a>tipo de recurso managementConditionStatement

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Una instrucción de condición de administración es un grupo de condiciones de administración que habilitar o deshabilitar las configuraciones de dispositivo o la aplicación cuando se cumplen todas las condiciones de administración contenido.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista managementConditionStatements](../api/intune-fencing-managementconditionstatement-list.md)|colección de [managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md)|Propiedades de la lista y relaciones de los objetos [managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md) .|
|[Obtener managementConditionStatement](../api/intune-fencing-managementconditionstatement-get.md)|[managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md)|Leer las propiedades y las relaciones del objeto [managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md) .|
|[Crear managementConditionStatement](../api/intune-fencing-managementconditionstatement-create.md)|[managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md)|Crear un nuevo objeto [managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md) .|
|[Eliminar managementConditionStatement](../api/intune-fencing-managementconditionstatement-delete.md)|Ninguno|Elimina un [managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md).|
|[Actualizar managementConditionStatement](../api/intune-fencing-managementconditionstatement-update.md)|[managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md)|Actualizar las propiedades de un objeto [managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md) .|
|[getManagementConditionStatementExpressionString (función)](../api/intune-fencing-managementconditionstatement-getmanagementconditionstatementexpressionstring.md)|[managementConditionExpressionString](../resources/intune-fencing-managementconditionexpressionstring.md)|Todavía no documentado|
|[getManagementConditionStatementsForPlatform (función)](../api/intune-fencing-managementconditionstatement-getmanagementconditionstatementsforplatform.md)|colección de [managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md)|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Identificador único de la instrucción de condición de administración. Valor asignado al crear generada por el sistema.|
|displayName|Cadena|El nombre definido de administración de la instrucción de condición de administración.|
|descripción|Cadena|El administrador define la descripción de la instrucción de condición de administración.|
|createdDateTime|DateTimeOffset|La hora en que se creó la instrucción de condición de administración. Servicio generado al lado.|
|modifiedDateTime|DateTimeOffset|La hora en que se modificó por última vez la instrucción de condición de administración. Se actualizó el lado de servicio.|
|expresión|[managementConditionExpression](../resources/intune-fencing-managementconditionexpression.md)|La expresión de instrucción de condición de administración que se usa para evaluar si una administración condición instrucción estaba activada o desactivada.|
|eTag|Cadena|ETag de la instrucción de condición de administración. Se actualizó el lado de servicio.|
|applicablePlatforms|colección de [devicePlatformType](../resources/intune-shared-deviceplatformtype.md)|Las plataformas aplicables para esta instrucción de condición de administración.
Esto se calcula a partir de ¿está buscando las condiciones de administración asociadas a la administración de la condición de la instrucción y buscar la intersección de plataformas aplicables.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Description|
|:---|:---|:---|
|managementConditions|colección de [managementCondition](../resources/intune-fencing-managementcondition.md)|Las condiciones de administración que se asocia a la instrucción de condición de administración.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managementConditionStatement"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managementConditionStatement",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "createdDateTime": "String (timestamp)",
  "modifiedDateTime": "String (timestamp)",
  "expression": {
    "@odata.type": "microsoft.graph.managementConditionExpression"
  },
  "eTag": "String",
  "applicablePlatforms": [
    "String"
  ]
}
```





