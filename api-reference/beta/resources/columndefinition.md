---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: ColumnDefinition
ms.openlocfilehash: 9b99abe78b009786d489ec7f0c0fdce1e2945b1d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083279"
---
# <a name="columndefinition-resource-type"></a>tipo de recurso columnDefinition

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

## <a name="json-representation"></a>Representación JSON

Aquí es una representación JSON de un recurso columnDefinition.

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.columnDefinition"
}-->

```json
{
  "columnGroup": "string",
  "description": "description",
  "displayName": "friendly name",
  "enforceUniqueValues": "true",
  "hidden": false,
  "id": "string",
  "indexed": true,
  "name": "staticNameForApi",
  "readOnly": false,
  "required": false,
  "boolean": { "@odata.type": "microsoft.graph.booleanColumn" },
  "calculated": { "@odata.type": "microsoft.graph.calculatedColumn" },
  "choice": { "@odata.type": "microsoft.graph.choiceColumn" },
  "currency": { "@odata.type": "microsoft.graph.currencyColumn" },
  "dateTime": { "@odata.type": "microsoft.graph.dateTimeColumn" },
  "defaultValue": { "@odata.type": "microsoft.graph.defaultColumnValue" },
  "geolocation": { "@odata.type": "microsoft.graph.geolocationColumn" },
  "lookup": { "@odata.type": "microsoft.graph.lookupColumn" },
  "number": { "@odata.type": "microsoft.graph.numberColumn" },
  "personOrGroup": { "@odata.type": "microsoft.graph.personOrGroupColumn" },
  "text": { "@odata.type": "microsoft.graph.textColumn" }
}
```

## <a name="properties"></a>Propiedades

Las columnas pueden contener datos de distintos tipos.
Las propiedades siguientes indican qué tipo de datos almacena una columna, así como una configuración adicional para esos datos.
Las propiedades relacionadas con el tipo (boolean, calculado, elección, moneda, fecha y hora, búsqueda, número, personOrGroup, texto) son mutuamente excluyentes: una columna sólo puede tener uno de ellos especificado.

| Nombre de propiedad           | Tipo    | Descripción
|:------------------------|:--------|:-----------------------------------------
| **columnGroup**         | string  | Para las columnas de sitio, el nombre del grupo al que pertenece esta columna. Ayuda a organizar las columnas relacionadas.
| **description**         | string  | Descripción de cara al usuario de la columna.
| **displayName**         | string  | Nombre de cara al usuario de la columna.
| **enforceUniqueValues** | boolean | Si es true, dos elementos de la lista no pueden tener el mismo valor para esta columna.
| **hidden**              | boolean | Especifica si la columna se muestra en la interfaz de usuario.
| **id**                  | string  | El identificador único de la columna.
| **indexed**             | boolean | Especifica si los valores de columna se pueden usar para ordenar y buscar.
| **name**                | string  | El nombre de cara a la API de la columna tal como aparece en [fields][] en un recurso [listItem][]. Para el nombre de cara al usuario, consulte **displayName**.
| **readOnly**            | bool    | Especifica si se pueden modificar los valores de columna.
| **required**            | boolean | Especifica si el valor de columna no es opcional.
| **boolean**       | [booleanColumn][]       | Esta columna almacena valores booleanos.
| **calculated**    | [calculatedColumn][]    | Los datos de la columna se calculan en función de otras columnas.
| **choice**        | [choiceColumn][]        | Esta columna almacena los datos de una lista de opciones.
| **currency**      | [currencyColumn][]      | Esta columna almacena valores de moneda.
| **dateTime**      | [dateTimeColumn][]      | Esta columna almacena valores DateTime.
| **defaultValue**  | [defaultColumnValue][]  | El valor predeterminado de esta columna.
| **ubicación geográfica**   | [geolocationColumn][]   | Esta columna almacena una ubicación geográfica.
| **lookup**        | [lookupColumn][]        | Los datos de esta columna se buscan desde otro origen en el sitio.
| **number**        | [numberColumn][]        | Esta columna almacena valores de números.
| **personOrGroup** | [personOrGroupColumn][] | Esta columna almacena valores de personas o grupos.
| **text**          | [textColumn][]          | Esta columna almacena valores de texto.

>**Nota:** Estas propiedades corresponden a la enumeración de [SPFieldType][] de SharePoint.
Mientras se representan los tipos más comunes de campo en la tabla anterior, esta versión beta API aún faltan algunos.
En esos casos, no se rellenará ninguna de las facetas de tipo de columna y la columna solo tendrá sus propiedades básicas.

## <a name="remarks"></a>Comentarios

De forma predeterminada, las ColumnDefinitions y los valores de campo de las columnas `hidden` no se muestran.
Para verlas al enumerar las **columnDefinitions**, incluya `hidden` en su instrucción `$select`.
Para verlas al mostrar los valores de **campo** en [listItems][listItem], incluya las columnas que quiera por nombre en su instrucción `$select`.

[booleanColumn]: booleancolumn.md
[calculatedColumn]: calculatedcolumn.md
[choiceColumn]: choicecolumn.md
[currencyColumn]: currencycolumn.md
[dateTimeColumn]: datetimecolumn.md
[defaultColumnValue]: defaultcolumnvalue.md
[geolocationColumn]: geolocationcolumn.md
[lookupColumn]: lookupcolumn.md
[numberColumn]: numbercolumn.md
[personOrGroupColumn]: personorgroupcolumn.md
[textColumn]: textcolumn.md
[fieldValueSet]: fieldvalueset.md
[fields]: fieldvalueset.md
[listItem]: listitem.md

[SPFieldType]: https://msdn.microsoft.com/library/microsoft.sharepoint.spfieldtype.aspx

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/ColumnDefinition"
} -->
