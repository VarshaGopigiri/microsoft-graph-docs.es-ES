---
title: Tipo de recurso recurrencePattern
description: 'Describe la frecuencia con la que se repite un evento periódico. '
localization_priority: Normal
ms.openlocfilehash: ebdb8a71d9f3acfb40191a7148f55999f6158aa1
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27892186"
---
# <a name="recurrencepattern-resource-type"></a>Tipo de recurso recurrencePattern

Describe la frecuencia con la que se repite un [evento](event.md) periódico. 

Puede especificar el patrón de periodicidad de un evento periódico siguiendo uno de los seis métodos según su situación. Para cada tipo de patrón, especifique la cantidad de tiempo entre las repeticiones. Las repeticiones actuales del evento periódico siempre seguirán este patrón, y se limitarán al intervalo de fechas que especifique para el evento. Un evento periódico siempre se define por su valor **recurrencePattern** (con qué frecuencia se repite el evento) y su valor [recurrenceRange](recurrencerange.md) (durante cuánto tiempo se repite el evento).

Use la propiedad **type** para especificar los diferentes tipos de **recurrencePattern** y la propiedad **interval** para especificar el tiempo entre las repeticiones. Puede hacerlo de varios modos: especificando días, semanas, meses o años en función del valor **type**. Tenga en cuenta las propiedades necesarias para cada tipo, tal como se describe en la tabla siguiente.

> **Nota**: Incluya únicamente las propiedades que necesita para un patrón de periodicidad. Cualquier propiedad que incluya que no tenga un valor admitido hará que se produzca un error.

| Tipo de patrón de periodicidad | Valor de la propiedad type | Descripción | Ejemplo | Propiedades requeridas |
|:---------------|:--------|:--------|:--------|:----------|
| Diario | `daily` | El evento se repite según el número de días especificados en el valor **interval** entre repeticiones. | Repita el evento cada tres días. | **type**, **interval** |
| Semanal | `weekly` | El evento se repetirá el mismo día o los mismos días de la semana, en función del número de semanas entre cada conjunto de repeticiones. | Repita el evento los lunes y martes de cada dos semanas. | **type**, **interval**, **daysOfWeek**, **firstDayOfWeek** |
| Mensual absoluto | `absoluteMonthly` | El evento se repite el día del mes especificado (por ejemplo, el día 15), en función del número de meses entre las repeticiones. | Repita este evento de forma trimestral (cada tres meses) el día 15. | **type**, **interval**, **dayOfMonth** |
| Mensual relativo | `relativeMonthly` | El evento se repite el día o los días de la semana especificados, en la misma posición relativa del mes, en función del número de meses entre las repeticiones. | Repita el evento el segundo jueves y viernes de cada trimestre. | **type**, **interval**, **daysOfWeek** |
| Anual absoluto | `absoluteYearly` | El evento se repite el día y el mes especificados, en función del número de años entre repeticiones. | Repita el evento el 15 de marzo cada tres meses. | **type**, **interval**, **dayOfMonth**, **month** |
| Anual relativo | `relativeYearly` | El evento se repite el día o los días de la semana especificados, en la misma posición relativa del mes del año específico, en función del número de años entre repeticiones. | Repita el evento el segundo jueves y viernes de noviembre cada tres años. | **type**, **interval**, **daysOfWeek**, **month** |


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|dayOfMonth|Int32|Día del mes en el que se produce el evento. Se requiere si **type** es `absoluteMonthly` o `absoluteYearly`. |
|daysOfWeek|colección de dayOfWeek|Colección de los días de la semana en los que se produce el evento. Los valores posibles son: `sunday`, `monday`, `tuesday`, `wednesday`, `thursday`, `friday`, `saturday`. <br>Si **type** es `relativeMonthly` o `relativeYearly`, y **daysOfWeek** especifica más de un día, el evento ocurre en el primer día que cumpla con el patrón. <br> Se requiere si **type** es `weekly`, `relativeMonthly` o `relativeYearly`.|
|firstDayOfWeek|dayOfWeek|Primer día de la semana. Los valores posibles son: `sunday`, `monday`, `tuesday`, `wednesday`, `thursday`, `friday`, `saturday`. El valor predeterminado es `sunday`. Se requiere si **type** es `weekly`. |
|index|weekIndex|Especifica en qué instancia de los días permitidos especificados en **daysOfsWeek** se produce el evento, contados a partir de la primera instancia del mes. Los valores posibles son: `first`, `second`, `third`, `fourth`, `last`. El valor predeterminado es `first`. Es opcional y se usa si **type** es `relativeMonthly` o `relativeYearly`. |
|interval|Int32|El número de unidades entre repeticiones, donde las unidades pueden ser días, semanas, meses o años, dependiendo de **type**. Obligatorio. |
|mes|Int32|Mes en el que se produce el evento.  Se trata de un número entre 1 y 12.|
|type|recurrencePatternType|Tipo de patrón de periodicidad: `daily`, `weekly`, `absoluteMonthly`, `relativeMonthly`, `absoluteYearly`, `relativeYearly`. Obligatorio.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.recurrencePattern"
}-->

```json
{
  "dayOfMonth": 1024,
  "daysOfWeek": ["String"],
  "firstDayOfWeek": "String",
  "index": "String",
  "interval": 1024,
  "month": 1024,
  "type": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "recurrencePattern resource",
  "keywords": "",
  "section": "documentation",
  "suppressions": [
    "Warning: /api-reference/v1.0/resources/recurrencepattern.md/microsoft.graph.recurrencePattern/daysOfWeek:
      Inconsistent types between parameter (String) and table (Object)"
  ],
  "tocPath": ""
}-->
