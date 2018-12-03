---
title: Programar citas repetidas como eventos periódicos en Outlook
description: Los eventos periódicos son una parte importante del Calendario de Outlook. Ya sea una reunión semanal personal con su jefe o una reunión de revisión de todo un departamento que tiene lugar el segundo martes de cada mes, los eventos periódicos facilitan la tarea al crear el evento una sola vez y que el servidor complete el resto de la serie.
ms.openlocfilehash: 1af082a32d79f6011e93a7fc0c5fc9d553d16712
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092779"
---
# <a name="schedule-repeating-appointments-as-recurring-events-in-outlook"></a>Programar citas repetidas como eventos periódicos en Outlook

Los eventos periódicos son una parte importante del Calendario de Outlook. Ya sea una reunión semanal personal con su jefe o una reunión de revisión de todo un departamento que tiene lugar el segundo martes de cada mes, los eventos periódicos facilitan la tarea al crear el evento una sola vez y que el servidor complete el resto de la serie.

La clave de información que permite a los eventos periódicos "expandirse" en las repeticiones periódicas individuales es la regla de periodicidad. La regla especifica con qué frecuencia se repite un evento y durante cuánto tiempo. Las API de REST de Outlook definen las reglas de periodicidad en la propiedad **recurrence** del [recurso de evento](/graph/api/resources/event?view=graph-rest-1.0). 

Cada recurrencia se compone de dos partes: el patrón de periodicidad (la frecuencia) y el intervalo de periodicidad (la duración).

## <a name="recurrence-patterns"></a>Patrones de periodicidad

La primera parte de una repetición es el patrón. Especifica la frecuencia con que se repite el evento. Por ejemplo, un evento podría repetirse "cada 3 días", "todos los jueves" o "el 22 de julio de cada año". Un patrón se representa en la API con el [recurso recurrencePattern](/graph/api/resources/recurrencepattern?view=graph-rest-1.0).

Según el tipo de patrón, ciertos campos de **recurrencePattern** son obligatorios, opcionales u omitidos.

> **Nota**: Incluso si se omite un campo, también se valida. Si un campo tiene una lista determinada de valores posibles, utilizar un valor fuera del conjunto permitido provocará un error, incluso si ese campo se omite.

Analicemos cada uno de los tipos de patrones posibles.

### <a name="daily"></a>Diario

El patrón de periodicidad diario hace que se repita basándose en el número de días que transcurre entre cada evento.

#### <a name="relevant-properties"></a>Propiedades relevantes

| Propiedad | Relevancia | Descripción |
|----------|-----------|-------------|
| **interval** | Obligatorio | Especifica el número de días entre cada repetición. |
| **type** | Obligatorio | Se debe establecer en `daily`. |

#### <a name="examples"></a>Ejemplos

- Repetir este evento cada día

  ```json
    "pattern": {
      "type": "daily",
      "interval": 1
    }
  ```
- Repetir este evento cada tres días

  ```json
    "pattern": {
      "type": "daily",
      "interval": 3
    }
  ```

### <a name="weekly"></a>Semanal

El patrón de periodicidad semanal provoca que un evento se repita en el mismo día o días de la semana, en función del número de semanas que transcurren entre cada conjunto de eventos.

#### <a name="relevant-properties"></a>Propiedades relevantes

| Propiedad | Relevancia | Descripción |
|----------|-----------|-------------|
| **daysOfWeek** | Obligatorio | Especifica en qué días de la semana se produce el evento. |
| **firstDayOfWeek** | Opcional | Especifica qué día se considera el primer día de la semana. Valor predeterminado: `Sunday`. |
| **interval** | Obligatorio | Especifica el número de semanas entre cada conjunto de eventos. |
| **type** | Obligatorio | Se debe establecer en `weekly`. |

#### <a name="examples"></a>Ejemplos

- Repetir este evento cada jueves

  ```json
    "pattern": {
      "type": "weekly",
      "interval": 1,
      "daysOfWeek": [ "Thursday" ]
    }
  ```
- Repetir este evento lunes y martes cada dos semanas

  ```json
    "pattern": {
      "type": "weekly",
      "interval": 2,
      "daysOfWeek": [
        "Monday",
        "Tuesday"
      ]
    }
  ```

### <a name="absolute-monthly"></a>Mensual absoluto

El patrón mensual absoluto hace que un evento se repita el mismo día del mes (por ejemplo, el día 15), en función del número de meses entre cada repetición.

#### <a name="relevant-properties"></a>Propiedades relevantes

| Propiedad | Relevancia | Descripción |
|----------|-----------|-------------|
| **dayOfMonth** | Obligatorio | Especifica el día del mes en que se produce el evento. |
| **interval** | Obligatorio | Especifica el número de meses entre cada repetición. |
| **type** | Obligatorio | Se debe establecer en `absoluteMonthly`. |

#### <a name="examples"></a>Ejemplos

- Repetir este evento el día 15 de cada mes

  ```json
    "pattern": {
      "type": "absoluteMonthly",
      "interval": 1,
      "dayOfMonth": 15
    }
  ```
- Repetir este evento trimestralmente (cada 3 meses) el día 7

  ```json
    "pattern": {
      "type": "absoluteMonthly",
      "interval": 3,
      "dayOfMonth": 7
    }
  ```

### <a name="relative-monthly"></a>Mensual relativo

El patrón mensual relativo hace que un evento se repita el mismo día de la semana en la misma posición relativa en el mes, en función del número de meses entre cada repetición. Por ejemplo, "cada segundo miércoles del mes".

#### <a name="relevant-properties"></a>Propiedades relevantes

| Propiedad | Relevancia | Descripción |
|----------|-----------|-------------|
| **daysOfWeek** | Obligatorio | Especifica en qué días de la semana puede producirse el evento. Los eventos mensuales relativos sólo ocurren una vez al mes, por lo que si especifica más de un valor, el evento tendrá lugar en el primer día que se ajuste al patrón. |
| **index** | Opcional | Especifica en qué instancia de los días permitidos especificados en **daysOfsWeek** se produce el evento, contados a partir de la primera instancia del mes. Valores posibles: `first`, `second`, `third`, `fourth` y `last`. Valor predeterminado: `first`. |
| **interval** | Obligatorio | Especifica el número de meses entre cada repetición. |
| **type** | Obligatorio | Se debe establecer en `relativeMonthly`. |

#### <a name="examples"></a>Ejemplos

- Repetir este evento el segundo miércoles de cada mes

  ```json
    "pattern": {
      "type": "relativeMonthly",
      "interval": 1,
      "daysOfWeek": [ "Wednesday" ],
      "index": "second"
    }
  ```
- Repetir este evento en el primer jueves o viernes de cada mes

  ```json
    "pattern": {
      "type": "relativeMonthly",
      "interval": 1,
      "daysOfWeek": [ "Thursday", "Friday" ],
      "index": "first"
    }
  ```

### <a name="absolute-yearly"></a>Anual absoluto

El patrón anual absoluto hace que un evento se repita en el mismo mes y día (por ejemplo, 15 de abril), basándose en el número de años entre cada repetición.

#### <a name="relevant-properties"></a>Propiedades relevantes

| Propiedad | Relevancia | Descripción |
|----------|-----------|-------------|
| **dayOfMonth** | Obligatorio | Especifica el día del mes en que se produce el evento. |
| **month** | Obligatorio | Especifica en qué mes se produce el evento. |
| **interval** | Obligatorio | Especifica el número de años entre cada repetición. |
| **type** | Obligatorio | Se debe establecer en `absoluteYearly`. |

#### <a name="example"></a>Ejemplo

- Repetir este evento el 15 de abril de cada año

  ```json
    "pattern": {
      "type": "absoluteYearly",
      "interval": 1,
      "dayOfMonth": 15,
      "month": 4
    }
  ```

### <a name="relative-yearly"></a>Anual relativo

El patrón anual relativo hace que un evento se repita el mismo día de la semana en la misma posición relativa de un mes concreto, en función del número de años entre cada repetición. Por ejemplo, "cada último miércoles de noviembre".

#### <a name="relevant-properties"></a>Propiedades relevantes

| Propiedad | Relevancia | Descripción |
|----------|-----------|-------------|
| **daysOfWeek** | Obligatorio | Especifica en qué días de la semana puede producirse el evento. Los eventos anuales relativos sólo ocurren una vez al año, por lo que si especifica más de un valor, el evento tendrá lugar en el primer día que se ajuste al patrón. |
| **index** | Opcional | Especifica en qué instancia de los días permitidos especificados en **daysOfsWeek** se produce el evento, contados a partir de la primera instancia del mes. Valores posibles: `first`, `second`, `third`, `fourth` y `last`. Valor predeterminado: `first`. |
| **month** | Obligatorio | Especifica en qué mes se produce el evento. |
| **interval** | Obligatorio | Especifica el número de años entre cada repetición. |
| **type** | Obligatorio | Se debe establecer en `relativeMonthly`. |

#### <a name="examples"></a>Ejemplos

- Repetir este evento el último miércoles de noviembre de cada año

  ```json
    "pattern": {
      "type": "relativeYearly",
      "interval": 1,
      "daysOfWeek": [ "Wednesday" ],
      "index": "last",
      "month": 11
    }
  ```

## <a name="recurrence-ranges"></a>Intervalos de periodicidad

La segunda parte de una repetición es el rango. Especifica cuánto tiempo se repite el patrón. Por ejemplo, un evento podría terminar después de 10 repeticiones, en una fecha específica, o podría no tener fin. Un intervalo se representa en la API por el [recurso recurrenceRange](/graph/api/resources/recurrencepattern?view=graph-rest-1.0).

Según el tipo de intervalo, ciertos campos de **recurrenceRange** son obligatorios o ignorados.

> **Nota**: Incluso si se omite un campo, también se valida. Si un campo tiene una lista determinada de valores posibles, utilizar un valor fuera del conjunto permitido provocará un error, incluso si ese campo se omite.

Analicemos cada uno de los tipos de intervalo posibles.

### <a name="numbered-range"></a>Rango numerado

El rango numerado hace que un evento se produzca un número fijo de veces (según el modelo) desde la fecha de inicio.

#### <a name="relevant-properties"></a>Propiedades relevantes

| Propiedad | Relevancia | Descripción |
|----------|-----------|-------------|
| **numberOfOccurences** | Obligatorio | Especifica el número de repeticiones. Debe ser un número entero positivo. |
| **recurrenceTimeZone** | Opcional | Especifica la zona horaria de la propiedad **startDate**. Si no se especifica, se usa la zona horaria del evento. |
| **startDate** | Obligatorio | Especifica la fecha para comenzar a aplicar el patrón. El valor de **startDate** DEBE corresponderse con el valor de la fecha de la propiedad **start** en el [recurso de evento](/graph/api/resources/event?view=graph-rest-1.0). Tenga en cuenta que no puede producirse la primera aparición de la reunión en esta fecha si no encaja en el patrón. |
| **type** | Obligatorio | Se debe establecer en `numbered`. |

#### <a name="examples"></a>Ejemplos

- Repetir este evento 10 veces

  ```json
    "range": {
      "type": "numbered",
      "startDate": "2017-04-02",
      "numberOfOccurrences": 10
    }
  ```

### <a name="end-date-range"></a>Intervalo de fecha de finalización

El intervalo de fecha de finalización hace que un evento se repita todos los días que encajan en el patrón aplicable entre una fecha inicial y una fecha de finalización.

#### <a name="relevant-properties"></a>Propiedades relevantes

| Propiedad | Relevancia | Descripción |
|----------|-----------|-------------|
| **endDate** | Obligatorio | Especifica la fecha para dejar de aplicar el patrón. Tenga en cuenta que no puede producirse la última aparición de la reunión en esta fecha si no encaja en el patrón. |
| **recurrenceTimeZone** | Opcional | Especifica la zona horaria de las propiedades **startDate** y **endDate**. Si no se especifica, se usa la zona horaria del evento. |
| **startDate** | Obligatorio | Especifica la fecha para comenzar a aplicar el patrón. El valor de **startDate** DEBE corresponderse con el valor de la fecha de la propiedad **start** en el [recurso de evento](/graph/api/resources/event?view=graph-rest-1.0). Tenga en cuenta que no puede producirse la primera aparición de la reunión en esta fecha si no encaja en el patrón. |
| **type** | Obligatorio | Se debe establecer en **endDate**. |

#### <a name="examples"></a>Ejemplos

- Repetir este evento desde el 1 de julio de 2017 hasta el 31 de julio de 2017

  ```json
    "range": {
      "type": "endDate",
      "startDate": "2017-07-01",
      "endDate": "2017-07-31"
    }
  ```

### <a name="no-end-range"></a>Sin fecha de finalización

Sin fecha de finalización hace que un evento se repita todos los días que encajen en el patrón aplicable después de una fecha de inicio.

#### <a name="relevant-properties"></a>Propiedades relevantes

| Propiedad | Relevancia | Descripción |
|----------|-----------|-------------|
| **recurrenceTimeZone** | Opcional | Especifica la zona horaria de la propiedad **startDate**. Si no se especifica, se usa la zona horaria del evento. |
| **startDate** | Obligatorio | Especifica la fecha para comenzar a aplicar el patrón. El valor de **startDate** DEBE corresponderse con el valor de la fecha de la propiedad **start** en el [recurso de evento](/graph/api/resources/event?view=graph-rest-1.0). Tenga en cuenta que no puede producirse la primera aparición de la reunión en esta fecha si no encaja en el patrón. |
| **type** | Obligatorio | Se debe establecer en `noEnd`. |

#### <a name="examples"></a>Ejemplos

- Repetir este evento desde 15 de mayo de 2017 para siempre

  ```json
    "range": {
      "type": "noEnd",
      "startDate": "2017-05-15"
    }
  ```

## <a name="using-patterns-and-ranges-to-create-recurring-events"></a>Usar patrones y rangos para crear eventos periódicos

Ahora que hemos visto los patrones y rangos por separado, analicemos cómo funcionan e interactúan con las propiedades **start** y **end** en el evento.

### <a name="creating-a-recurrence-rule"></a>Crear una regla de periodicidad

Para crear una regla de periodicidad, debe especificar tanto un patrón como un rango. Cualquier tipo de patrón puede funcionar con cualquier tipo de rango. A continuación, se muestran algunos ejemplos.

#### <a name="examples"></a>Ejemplos

- **Reunión de 13:00 a 13:30 todos los lunes a partir del 4 de septiembre de 2017 hasta el final del año**

  - El requisito "cada lunes" se cumple fácilmente por el tipo de patrón de periodicidad `weekly`.
  - El requisito "hasta el final del año" indica un tipo de intervalo de repetición `endDate`.

  ```json
    "recurrence": {
      "pattern": {
        "type": "weekly",
        "interval": 1,
        "daysOfWeek": [ "Monday" ]
      },
      "range": {
        "type": "endDate",
        "startDate": "2017-09-04",
        "endDate": "2017-12-31"
      }
    }
  ```

  Dado que el 31 de diciembre de 2017 es domingo, la última aparición en esta serie será el lunes 25 de diciembre.

- **Reunión de 14:00 a 15:00 el primer jueves de meses alternos a partir del 29 de agosto de 2017**

  - El requisito "primer jueves de meses alternos" se consigue estableciendo un patrón mensual relativo. La parte "de meses alternos" indica que **interval** debe establecerse en `2`.
  - Dado que no hay ningún requisito de fecha de finalización, puede usarse un tipo de rango `noEnd`.

  ```json
    "recurrence": {
      "pattern": {
        "type": "relativeMonthly",
        "interval": 2,
        "daysOfWeek": [ "Thursday" ],
        "index": "first"
      },
      "range": {
        "type": "noEnd",
        "startDate": "2017-08-29"
      }
    }
  ```

  Dado que el valor de **startDate** comienza tras el primer jueves de agosto, la primera aparición de esta serie será en septiembre.

## <a name="next-steps"></a>Pasos siguientes
    
Obtenga más información sobre la [integración con el Calendario de Outlook](outlook-calendar-concept-overview.md).
