---
title: Tipo de recurso Workbook
description: Workbook es el objeto de nivel superior que contiene los objetos de libro relacionados, como hojas de cálculo, tablas, intervalos, etc.
localization_priority: Priority
author: lumine2008
ms.prod: excel
ms.openlocfilehash: b4f0a439db5cc430e558f2d43215cb1c5c0f7779
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27913124"
---
# <a name="workbook-resource-type"></a>Tipo de recurso Workbook

Workbook es el objeto de nivel superior que contiene los objetos de libro relacionados, como hojas de cálculo, tablas, intervalos, etc.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbook"
}-->

```json
{
  "names": [{"@odata.type": "microsoft.graph.workbookNamedItem"}],
  "tables": [{"@odata.type": "microsoft.graph.workbookTable"}],
  "worksheets": [{"@odata.type": "microsoft.graph.workbookWorksheet"}]
}
```

## <a name="properties"></a>Propiedades
Ninguno

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Crear una sesión](../api/workbook-createsession.md) | [workbookSessionInfo](workbooksessioninfo.md) |Crear una sesión de libro para iniciar una sesión persistente o no persistente.|
|[Cerrar sesión](../api/workbook-closesession.md) | Ninguno |Cerrar una sesión existente.|
|[Actualizar sesión](../api/workbook-refreshsession.md) | Ninguno |Actualizar una sesión existente.|


## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|names|Colección de [WorkbookNamedItem](nameditem.md)|Representa una colección de elementos con nombre en el ámbito del libro (intervalos y constantes con nombre). Solo lectura.|
|tables|Colección de [WorkbookTable](table.md)|Representa una colección de tablas asociadas con el libro. Solo lectura.|
|worksheets|Colección de [WorkbookWorksheet](worksheet.md)|Representa una colección de hojas de cálculo asociadas con el libro. Solo lectura.|

## <a name="functions"></a>Funciones

[Funciones de Excel](#functions): Para invocar una función de libro, use la sintaxis `POST /workbook/functions/{function-name}` y proporcione los argumentos de la función en el cuerpo mediante un objeto JSON. Las cadenas `value` y `error` resultantes de la función se devuelven en el objeto de resultado de la función. El valor `error` de `null` indica que la función se ha ejecutado correctamente. 

La lista completa de funciones admitidas se encuentra [aquí](https://support.office.com/en-us/article/Excel-functions-alphabetical-b3944572-255d-4efb-bb96-c6d90033e188). Consulte la firma de la función para obtener tipos de datos y nombres de parámetros específicos.

_Notas importantes:_ 
* El parámetro de entrada de intervalo se suministra mediante un objeto range en lugar de la cadena de dirección de intervalo.  
* El parámetro de índice es “1 indexado”, a diferencia del “índice 0” usado en la mayoría de las API. 

Ejemplo: **BUSCARV**

En una hoja de cálculo de Excel, la función `vlookup` admite estos argumentos:

1. El valor que quiere buscar, también llamado el valor de búsqueda.
2. El rango donde se encuentra el valor de búsqueda. Recuerde que el valor de búsqueda siempre tiene que estar en la primera columna del rango para que BUSCARV funcione correctamente. Por ejemplo, si el valor de búsqueda se encuentra en la celda C2, el rango tiene que empezar con C.
3. El número de columna en el rango que contiene el valor devuelto. Por ejemplo, si especifica B2:D11 como el rango, B será la primera columna, C la segunda, etc.
4. De forma opcional, puede especificar VERDADERO si quiere obtener una coincidencia aproximada, o bien FALSO si quiere obtener una coincidencia exacta del valor devuelto. Si no especifica nada, el valor predeterminado será siempre VERDADERO o coincidencia aproximada.

Dentro de una celda, la función `vlookup` es similar a esta: 

= BUSCARV(valor de búsqueda, rango que contiene el valor de búsqueda, el número de columna en el rango que contiene el valor devuelto, de forma opcional, especifique VERDADERO para obtener una coincidencia aproximada o FALSO para una coincidencia exacta)

(Vea la documentación de la [Función de Excel BUSCARV](https://support.office.com/en-us/article/VLOOKUP-function-0bbc8083-26fe-4963-8ab8-93a18ad188a1)).

En el ejemplo siguiente, se muestra cómo realizar una llamada a la función `vlookup` y pasar estos parámetros con la API de REST de Excel.

Solicitud: 

```http 
POST https://graph.microsoft.com/beta/me/drive/root:/book1.xlsx:/workbook/functions/vlookup
content-type: Application/Json 
authorization: Bearer {access-token} 
workbook-session-id: {session-id}

{
    "lookupValue": "Temperature",
    "tableArray": { "Address": "Sheet1!E1:G5" },
    "colIndexNum": 2,
    "rangeLookup": false
}
```

Respuesta:

```http
HTTP code: 200 OK
content-type: application/json;odata.metadata 

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#workbookFunctionResult",
    "@odata.type": "#microsoft.graph.workbookFunctionResult",
    "@odata.id": "/users('f6d92604-4b76-4b70-9a4c-93dfbcc054d5')/drive/root/workbook/functions/vlookup()",
    "error": null,
    "value": "28.3"
}
```

Ejemplo: `median`

En una hoja de cálculo de Excel, la función `median` admite una matriz de uno o más rangos de entrada.

Dentro de una celda, la función `median` es similar a este ejemplo:

=MEDIANA(A2:A6)

(Vea la documentación de la [Función de Excel MEDIANA](https://support.office.com/en-us/article/MEDIAN-function-d0916313-4753-414c-8537-ce85bdd967d2)).

En el ejemplo siguiente, se muestra cómo realizar una llamada a la función `median` y uno o más rangos de entrada con la API de REST de Excel. 

Solicitud: 

```http 
POST https://graph.microsoft.com/beta/me/drive/root:/book1.xlsx:/workbook/functions/median
content-type: Application/Json 
authorization: Bearer {access-token} 
workbook-session-id: {session-id}

{
"values" :  [
        { "address": "Sheet2!A1:A5" },
        { "address": "Sheet2!B1:B5" },
      ] 
}
```

Respuesta:

```http
HTTP code: 200 OK
content-type: application/json;odata.metadata 

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#workbookFunctionResult",
  "@odata.type": "#microsoft.graph.workbookFunctionResult",
  "@odata.id": "/users('2abcad6a-2fca-4b6e-9577-e358a757d77d')/drive/root/workbook/functions/median()",
  "error": null,
  "value": 30
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Workbook resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
