---
title: Tipo de recurso Workbook
description: Workbook es el objeto de nivel superior que contiene los objetos de libro relacionados, como hojas de cálculo, tablas, intervalos, etc.
localization_priority: Normal
ms.openlocfilehash: 9479c6888dc27fd595db2313ab6a88617410530f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27806800"
---
# <a name="workbook-resource-type"></a><span data-ttu-id="662b7-103">Tipo de recurso Workbook</span><span class="sxs-lookup"><span data-stu-id="662b7-103">Workbook resource type</span></span>

<span data-ttu-id="662b7-104">Workbook es el objeto de nivel superior que contiene los objetos de libro relacionados, como hojas de cálculo, tablas, intervalos, etc.</span><span class="sxs-lookup"><span data-stu-id="662b7-104">Workbook is the top level object which contains related workbook objects such as worksheets, tables, ranges, etc.</span></span>

## <a name="properties"></a><span data-ttu-id="662b7-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="662b7-105">Properties</span></span>
<span data-ttu-id="662b7-106">Ninguno</span><span class="sxs-lookup"><span data-stu-id="662b7-106">None</span></span>

## <a name="methods"></a><span data-ttu-id="662b7-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="662b7-107">Methods</span></span>

| <span data-ttu-id="662b7-108">Método</span><span class="sxs-lookup"><span data-stu-id="662b7-108">Method</span></span>       | <span data-ttu-id="662b7-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="662b7-109">Return Type</span></span>  |<span data-ttu-id="662b7-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="662b7-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="662b7-111">Crear una sesión</span><span class="sxs-lookup"><span data-stu-id="662b7-111">Create Session</span></span>](../api/workbook-createsession.md) | [<span data-ttu-id="662b7-112">workbookSessionInfo</span><span class="sxs-lookup"><span data-stu-id="662b7-112">workbookSessionInfo</span></span>](workbooksessioninfo.md) |<span data-ttu-id="662b7-113">Crear una sesión de libro para iniciar una sesión persistente o no persistente.</span><span class="sxs-lookup"><span data-stu-id="662b7-113">Create a workbook session to start a persistent or non-persistent session.</span></span>|
|[<span data-ttu-id="662b7-114">Cerrar sesión</span><span class="sxs-lookup"><span data-stu-id="662b7-114">Close Session</span></span>](../api/workbook-closesession.md) | <span data-ttu-id="662b7-115">Ninguno</span><span class="sxs-lookup"><span data-stu-id="662b7-115">None</span></span> |<span data-ttu-id="662b7-116">Cerrar una sesión existente.</span><span class="sxs-lookup"><span data-stu-id="662b7-116">Close an existing session.</span></span>|
|[<span data-ttu-id="662b7-117">Actualizar sesión</span><span class="sxs-lookup"><span data-stu-id="662b7-117">Refresh Session</span></span>](../api/workbook-refreshsession.md) | <span data-ttu-id="662b7-118">Ninguno</span><span class="sxs-lookup"><span data-stu-id="662b7-118">None</span></span> |<span data-ttu-id="662b7-119">Actualizar una sesión existente.</span><span class="sxs-lookup"><span data-stu-id="662b7-119">Refresh an existing session.</span></span>|


## <a name="relationships"></a><span data-ttu-id="662b7-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="662b7-120">Relationships</span></span>
| <span data-ttu-id="662b7-121">Relación</span><span class="sxs-lookup"><span data-stu-id="662b7-121">Relationship</span></span> | <span data-ttu-id="662b7-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="662b7-122">Type</span></span>   |<span data-ttu-id="662b7-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="662b7-123">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="662b7-124">names</span><span class="sxs-lookup"><span data-stu-id="662b7-124">names</span></span>|<span data-ttu-id="662b7-125">Colección [NamedItem](nameditem.md)</span><span class="sxs-lookup"><span data-stu-id="662b7-125">[NamedItem](nameditem.md) collection</span></span>|<span data-ttu-id="662b7-p101">Representa una colección de elementos con nombre en el ámbito del libro (intervalos y constantes con nombre). Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="662b7-p101">Represents a collection of workbook scoped named items (named ranges and constants). Read-only.</span></span>|
|<span data-ttu-id="662b7-128">tables</span><span class="sxs-lookup"><span data-stu-id="662b7-128">tables</span></span>|<span data-ttu-id="662b7-129">Colección [Table](table.md)</span><span class="sxs-lookup"><span data-stu-id="662b7-129">[Table](table.md) collection</span></span>|<span data-ttu-id="662b7-p102">Representa una colección de tablas asociadas con el libro. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="662b7-p102">Represents a collection of tables associated with the workbook. Read-only.</span></span>|
|<span data-ttu-id="662b7-132">worksheets</span><span class="sxs-lookup"><span data-stu-id="662b7-132">worksheets</span></span>|<span data-ttu-id="662b7-133">Colección [Worksheet](worksheet.md)</span><span class="sxs-lookup"><span data-stu-id="662b7-133">[Worksheet](worksheet.md) collection</span></span>|<span data-ttu-id="662b7-p103">Representa una colección de hojas de cálculo asociadas con el libro. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="662b7-p103">Represents a collection of worksheets associated with the workbook. Read-only.</span></span>|

## <a name="functions"></a><span data-ttu-id="662b7-136">Funciones</span><span class="sxs-lookup"><span data-stu-id="662b7-136">Functions</span></span>

<span data-ttu-id="662b7-p104">[Funciones de Excel](#functions): Para invocar una función de libro, use la sintaxis `POST /workbook/functions/{function-name}` y proporcione los argumentos de la función en el cuerpo mediante un objeto JSON. Las cadenas `value` y `error` resultantes de la función se devuelven en el objeto de resultado de la función. El valor `error` de `null` indica que la función se ha ejecutado correctamente.</span><span class="sxs-lookup"><span data-stu-id="662b7-p104">[Excel functions](#functions): Invoke a workbook function using the syntax `POST /workbook/functions/{function-name}` and providing the function argument(s) in the body using a JSON object. The function's resulting `value` and any `error` strings are returned in the function result object. The `error` value of `null` indicates successful execution of the function.</span></span> 

<span data-ttu-id="662b7-p105">La lista completa de funciones admitidas se encuentra [aquí](https://support.office.com/en-us/article/Excel-functions-alphabetical-b3944572-255d-4efb-bb96-c6d90033e188). Consulte la firma de la función para obtener tipos de datos y nombres de parámetros específicos.</span><span class="sxs-lookup"><span data-stu-id="662b7-p105">The complete list of supported functions are listed [here](https://support.office.com/en-us/article/Excel-functions-alphabetical-b3944572-255d-4efb-bb96-c6d90033e188). Refer to the function signature for specific parameter names and data types.</span></span>

<span data-ttu-id="662b7-142">_Notas importantes:_</span><span class="sxs-lookup"><span data-stu-id="662b7-142">_Important notes:_</span></span> 
* <span data-ttu-id="662b7-143">El parámetro de entrada de intervalo se suministra mediante un objeto range en lugar de la cadena de dirección de intervalo.</span><span class="sxs-lookup"><span data-stu-id="662b7-143">The range input parameter is supplied using a range object instead of the range address string.</span></span>  
* <span data-ttu-id="662b7-144">El parámetro de índice es “1 indexado”, a diferencia del “índice 0” usado en la mayoría de las API.</span><span class="sxs-lookup"><span data-stu-id="662b7-144">The index parameter is 1-indexed unlike the 0-index used in most of the APIs.</span></span> 

<span data-ttu-id="662b7-145">Ejemplo: **BUSCARV**</span><span class="sxs-lookup"><span data-stu-id="662b7-145">Example: **vlookup**</span></span>

<span data-ttu-id="662b7-146">En una hoja de cálculo de Excel, la función `vlookup` admite estos argumentos:</span><span class="sxs-lookup"><span data-stu-id="662b7-146">In an Excel spreadsheet, the `vlookup` function takes the following arguments:</span></span>

1. <span data-ttu-id="662b7-147">El valor que quiere buscar, también llamado el valor de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="662b7-147">The value you want to look up, also called the lookup value.</span></span>
2. <span data-ttu-id="662b7-148">El rango donde se encuentra el valor de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="662b7-148">The range where the lookup value is located.</span></span> <span data-ttu-id="662b7-149">Recuerde que el valor de búsqueda siempre tiene que estar en la primera columna del rango para que BUSCARV funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="662b7-149">Remember that the lookup value should always be in the first column in the range for VLOOKUP to work correctly.</span></span> <span data-ttu-id="662b7-150">Por ejemplo, si el valor de búsqueda se encuentra en la celda C2, el rango tiene que empezar con C.</span><span class="sxs-lookup"><span data-stu-id="662b7-150">For example, if your lookup value is in cell C2 then your range should start with C.</span></span>
3. <span data-ttu-id="662b7-151">El número de columna en el rango que contiene el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="662b7-151">The column number in the range that contains the return value.</span></span> <span data-ttu-id="662b7-152">Por ejemplo, si especifica B2:D11 como el rango, B será la primera columna, C la segunda, etc.</span><span class="sxs-lookup"><span data-stu-id="662b7-152">For example, if you specify B2: D11 as the range, you should count B as the first column, C as the second, and so on.</span></span>
4. <span data-ttu-id="662b7-153">De forma opcional, puede especificar VERDADERO si quiere obtener una coincidencia aproximada, o bien FALSO si quiere obtener una coincidencia exacta del valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="662b7-153">Optionally, you can specify TRUE if you want an approximate match or FALSE if you want an exact match of the return value.</span></span> <span data-ttu-id="662b7-154">Si no especifica nada, el valor predeterminado será siempre VERDADERO o coincidencia aproximada.</span><span class="sxs-lookup"><span data-stu-id="662b7-154">If you don't specify anything, the default value will always be TRUE or approximate match.</span></span>

<span data-ttu-id="662b7-155">Dentro de una celda, la función `vlookup` es similar a esta:</span><span class="sxs-lookup"><span data-stu-id="662b7-155">Inside a cell, the `vlookup` function looks like this:</span></span> 

<span data-ttu-id="662b7-156">= BUSCARV(valor de búsqueda, rango que contiene el valor de búsqueda, el número de columna en el rango que contiene el valor devuelto, de forma opcional, especifique VERDADERO para obtener una coincidencia aproximada o FALSO para una coincidencia exacta)</span><span class="sxs-lookup"><span data-stu-id="662b7-156">=VLOOKUP(lookup value, range containing the lookup value, the column number in the range containing the return value, optionally specify TRUE for approximate match or FALSE for an exact match)</span></span>

<span data-ttu-id="662b7-157">(Vea la documentación de la [Función de Excel BUSCARV](https://support.office.com/en-us/article/VLOOKUP-function-0bbc8083-26fe-4963-8ab8-93a18ad188a1)).</span><span class="sxs-lookup"><span data-stu-id="662b7-157">(See the documentation for the [VLOOKUP Excel function](https://support.office.com/en-us/article/VLOOKUP-function-0bbc8083-26fe-4963-8ab8-93a18ad188a1).)</span></span>

<span data-ttu-id="662b7-158">En el ejemplo siguiente, se muestra cómo realizar una llamada a la función `vlookup` y pasar estos parámetros con la API de REST de Excel.</span><span class="sxs-lookup"><span data-stu-id="662b7-158">The example below shows how to call the `vlookup` function and pass these parameters with the Excel REST API.</span></span>
<span data-ttu-id="662b7-159">Solicitud:</span><span class="sxs-lookup"><span data-stu-id="662b7-159">Request:</span></span> 

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

<span data-ttu-id="662b7-160">Respuesta:</span><span class="sxs-lookup"><span data-stu-id="662b7-160">Response:</span></span>

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

<span data-ttu-id="662b7-161">Ejemplo: `median`</span><span class="sxs-lookup"><span data-stu-id="662b7-161">Example: `median`</span></span>

<span data-ttu-id="662b7-162">En una hoja de cálculo de Excel, la función `median` admite una matriz de uno o más rangos de entrada.</span><span class="sxs-lookup"><span data-stu-id="662b7-162">In an Excel spreadsheet, the `median` function takes an array of one or more input ranges.</span></span>

<span data-ttu-id="662b7-163">Dentro de una celda, la función `median` es similar a este ejemplo:</span><span class="sxs-lookup"><span data-stu-id="662b7-163">Inside a cell, the `median` function looks like this example:</span></span>

<span data-ttu-id="662b7-164">=MEDIANA(A2:A6)</span><span class="sxs-lookup"><span data-stu-id="662b7-164">=MEDIAN(A2:A6)</span></span>

<span data-ttu-id="662b7-165">(Vea la documentación de la [Función de Excel MEDIANA](https://support.office.com/en-us/article/MEDIAN-function-d0916313-4753-414c-8537-ce85bdd967d2)).</span><span class="sxs-lookup"><span data-stu-id="662b7-165">(See the documentation for the [MEDIAN Excel function](https://support.office.com/en-us/article/MEDIAN-function-d0916313-4753-414c-8537-ce85bdd967d2).)</span></span>

<span data-ttu-id="662b7-166">En el ejemplo siguiente, se muestra cómo realizar una llamada a la función `median` y uno o más rangos de entrada con la API de REST de Excel.</span><span class="sxs-lookup"><span data-stu-id="662b7-166">The example below shows how to call the `median` function and one or more input ranges with the Excel REST API.</span></span> 

<span data-ttu-id="662b7-167">Solicitud:</span><span class="sxs-lookup"><span data-stu-id="662b7-167">Request:</span></span> 

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

<span data-ttu-id="662b7-168">Respuesta:</span><span class="sxs-lookup"><span data-stu-id="662b7-168">Response:</span></span>

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
