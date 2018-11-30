---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: ColumnDefinition
ms.openlocfilehash: 96587cc1b3badf2d5fcc90bc7c1d2b1cfb710f6b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029467"
---
# <a name="columndefinition-resource"></a>Recurso ColumnDefinition

## <a name="json-representation"></a>Representación JSON

A continuación se incluye una representación JSON de un recurso ColumnDefinition.

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
  "lookup": { "@odata.type": "microsoft.graph.lookupColumn" },
  "number": { "@odata.type": "microsoft.graph.numberColumn" },
  "personOrGroup": { "@odata.type": "microsoft.graph.personOrGroupColumn" },
  "text": { "@odata.type": "microsoft.graph.textColumn" }
}
```

## <a name="properties"></a>Propiedades

El recurso **columnDefinition** tiene las siguientes propiedades.

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

Las columnas pueden contener datos de distintos tipos.
Las propiedades siguientes indican qué tipo de datos almacena una columna, así como una configuración adicional para esos datos.
Estas propiedades son mutuamente exclusivas, una columna solo puede tener uno de ellos especificados.

| Nombre de propiedad     | Tipo                    | Descripción
|:------------------|:------------------------|:-------------------------------
| **boolean**       | [booleanColumn][]       | Esta columna almacena valores booleanos.
| **calculated**    | [calculatedColumn][]    | Los datos de la columna se calculan en función de otras columnas.
| **choice**        | [choiceColumn][]        | Esta columna almacena los datos de una lista de opciones.
| **currency**      | [currencyColumn][]      | Esta columna almacena valores de moneda.
| **dateTime**      | [dateTimeColumn][]      | Esta columna almacena valores DateTime.
| **defaultValue**  | [defaultColumnValue][]  | El valor predeterminado de esta columna.
| **lookup**        | [lookupColumn][]        | Los datos de esta columna se buscan desde otro origen en el sitio.
| **number**        | [numberColumn][]        | Esta columna almacena valores de números.
| **personOrGroup** | [personOrGroupColumn][] | Esta columna almacena valores de personas o grupos.
| **text**          | [textColumn][]          | Esta columna almacena valores de texto.

Nota: Estas propiedades se corresponden con la enumeración [SPFieldType][] de SharePoint.
Mientras se representan los tipos más comunes de campo anteriormente, esta API es aún faltan algunos.
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
