---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: DateTimeColumn
ms.openlocfilehash: ce5f06b6e0d88324813372c2431b62e6b9105bcb
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="datetimecolumn-resource-type"></a>Tipo de recurso DateTimeColumn

El recurso **dateTimeColumn** en un recurso [columnDefinition](columnDefinition.md) indica que los valores de la columna son fechas u horas.

## <a name="json-representation"></a>Representación JSON

A continuación se incluye una representación JSON de un recurso **dateTimeColumn**.
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.dateTimeColumn" } -->

```json
{
  "displayAs": "default | friendly | standard",
  "format": "dateOnly | dateTime"
}
```

## <a name="properties"></a>Propiedades

| Nombre de la propiedad      | Tipo               | Descripción
|:-------------------|:-------------------|:----------------------------------------------
| **displayAs**      | string             | Cómo se debe presentar el valor en la experiencia de usuario. Debe ser `default`, `friendly` o `standard`. Vea lo que se muestra a continuación para obtener más detalles. Si no se especifica, se trata como `default`.
| **format**         | string             | Indica si el valor debe presentarse solo como una fecha o como fecha y hora. Debe ser `dateOnly` o `dateTime`

## <a name="displayas-values"></a>Valores displayAs

| Valor        | Descripción
|:-------------|:--------------------------------------------------------------
| **default**  | Usa la representación predeterminada de la experiencia de usuario.
| **friendly** | Usa una representación relativa descriptiva (p. ej., "hoy a las 15:00")
| **standard** | Usa la representación absoluta estándar (p. ej. "10/5/2017 15:20")


<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/DateTimeColumn"
} -->
