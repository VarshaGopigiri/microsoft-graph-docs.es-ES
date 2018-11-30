---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: DateTimeColumn
ms.openlocfilehash: 9854ad35c602ff474604f2ca88e7182c325e797d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083865"
---
# <a name="datetimecolumn-resource-type"></a>Tipo de recurso DateTimeColumn

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **dateTimeColumn** en un recurso [columnDefinition](columndefinition.md) indica que los valores de la columna son fechas u horas.

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

| Nombre de propiedad      | Tipo               | Descripción
|:-------------------|:-------------------|:----------------------------------------------
| **displayAs**      | string             | Cómo se debe presentar el valor en la experiencia de usuario. Debe ser `default`, `friendly` o `standard`. Vea lo que se muestra a continuación para obtener más detalles. Si no se especifica, se trata como `default`.
| **format**         | string             | Indica si el valor debe presentarse solo como una fecha o como fecha y hora. Debe ser `dateOnly` o `dateTime`

## <a name="displayas-values"></a>Valores displayAs

| Valor        | Descripción
|:-------------|:--------------------------------------------------------------
| **default**  | Usa la representación predeterminada de la experiencia de usuario.
| **friendly** | Usa una representación relativa descriptiva (p. ej., "hoy a las 3:00 p. m.")
| **standard** | Usa la representación absoluta estándar (p. ej. "5/10/2017 3:20 p. m.")


<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/DateTimeColumn"
} -->
