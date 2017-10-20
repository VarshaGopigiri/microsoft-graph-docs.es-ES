---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: ColumnDefinition
ms.openlocfilehash: e5942ddee4b505243cb64121862ce9e89e52d245
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="columndefinition-resource"></a>Recurso ColumnDefinition

## <a name="json-representation"></a>Representación JSON

A continuación se incluye una representación JSON de un recurso ColumnDefinition.

<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.columnDefinition",
       "keyProperty": "id", "optionalProperties": [ ] } -->

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
Aunque los tipos más comunes de campo están representados en la tabla anterior, aún faltan algunos en esta API de versión beta.
En esos casos, no se rellenará ninguna de las facetas de tipo de columna y la columna solo tendrá sus propiedades básicas.

## <a name="remarks"></a>Comentarios

De forma predeterminada, las ColumnDefinitions y los valores de campo de las columnas `hidden` no se muestran.
Para verlas al enumerar las **columnDefinitions**, incluya `hidden` en su instrucción `$select`.
Para verlas al mostrar los valores de **campo** en [listItems][listItem], incluya las columnas que quiera por nombre en su instrucción `$select`.

[booleanColumn]: booleanColumn.md
[calculatedColumn]: calculatedColumn.md
[choiceColumn]: choiceColumn.md
[currencyColumn]: currencyColumn.md
[dateTimeColumn]: dateTimeColumn.md
[defaultColumnValue]: defaultColumnValue.md
[lookupColumn]: lookupColumn.md
[numberColumn]: numberColumn.md
[personOrGroupColumn]: personOrGroupColumn.md
[textColumn]: textColumn.md
[fieldValueSet]: fieldValueSet.md
[fields]: fieldvalueset.md
[listItem]: listitem.md

[SPFieldType]: https://msdn.microsoft.com/en-us/library/microsoft.sharepoint.spfieldtype.aspx

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/ColumnDefinition"
} -->
