# <a name="workbook-resource-type"></a><span data-ttu-id="3bab0-101">Tipo de recurso Workbook</span><span class="sxs-lookup"><span data-stu-id="3bab0-101">Workbook resource type</span></span>

<span data-ttu-id="3bab0-102">Workbook es el objeto de nivel superior que contiene los objetos de libro relacionados, como hojas de cálculo, tablas, intervalos, etc.</span><span class="sxs-lookup"><span data-stu-id="3bab0-102">Workbook is the top level object which contains related workbook objects such as worksheets, tables, ranges, etc.</span></span>

## <a name="properties"></a><span data-ttu-id="3bab0-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3bab0-103">Properties</span></span>
<span data-ttu-id="3bab0-104">Ninguno</span><span class="sxs-lookup"><span data-stu-id="3bab0-104">None</span></span>

## <a name="methods"></a><span data-ttu-id="3bab0-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="3bab0-105">Methods</span></span>

| <span data-ttu-id="3bab0-106">Método</span><span class="sxs-lookup"><span data-stu-id="3bab0-106">Method</span></span>       | <span data-ttu-id="3bab0-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3bab0-107">Return Type</span></span>  |<span data-ttu-id="3bab0-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="3bab0-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="3bab0-109">Crear una sesión</span><span class="sxs-lookup"><span data-stu-id="3bab0-109">Create Session</span></span>](../api/workbook_createsession.md) | [<span data-ttu-id="3bab0-110">workbookSessionInfo</span><span class="sxs-lookup"><span data-stu-id="3bab0-110">workbookSessionInfo</span></span>](workbooksessioninfo.md) |<span data-ttu-id="3bab0-111">Crear una sesión de libro para iniciar una sesión persistente o no persistente.</span><span class="sxs-lookup"><span data-stu-id="3bab0-111">Create a workbook session to start a persistent or non-persistent session.</span></span>|
|[<span data-ttu-id="3bab0-112">Cerrar sesión</span><span class="sxs-lookup"><span data-stu-id="3bab0-112">Close Session</span></span>](../api/workbook_closesession.md) | <span data-ttu-id="3bab0-113">Ninguno</span><span class="sxs-lookup"><span data-stu-id="3bab0-113">None</span></span> |<span data-ttu-id="3bab0-114">Cerrar una sesión existente.</span><span class="sxs-lookup"><span data-stu-id="3bab0-114">Close an existing session.</span></span>|
|[<span data-ttu-id="3bab0-115">Actualizar sesión</span><span class="sxs-lookup"><span data-stu-id="3bab0-115">Refresh Session</span></span>](../api/workbook_refreshsession.md) | <span data-ttu-id="3bab0-116">Ninguno</span><span class="sxs-lookup"><span data-stu-id="3bab0-116">None</span></span> |<span data-ttu-id="3bab0-117">Actualizar una sesión existente.</span><span class="sxs-lookup"><span data-stu-id="3bab0-117">Refresh an existing session.</span></span>|


## <a name="relationships"></a><span data-ttu-id="3bab0-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="3bab0-118">Relationships</span></span>
| <span data-ttu-id="3bab0-119">Relación</span><span class="sxs-lookup"><span data-stu-id="3bab0-119">Relationship</span></span> | <span data-ttu-id="3bab0-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="3bab0-120">Type</span></span>   |<span data-ttu-id="3bab0-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="3bab0-121">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="3bab0-122">names</span><span class="sxs-lookup"><span data-stu-id="3bab0-122">names</span></span>|<span data-ttu-id="3bab0-123">Colección [NamedItem](nameditem.md)</span><span class="sxs-lookup"><span data-stu-id="3bab0-123">[NamedItem](nameditem.md) collection</span></span>|<span data-ttu-id="3bab0-p101">Representa una colección de elementos con nombre en el ámbito del libro (intervalos y constantes con nombre). Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3bab0-p101">Represents a collection of workbook scoped named items (named ranges and constants). Read-only.</span></span>|
|<span data-ttu-id="3bab0-126">tables</span><span class="sxs-lookup"><span data-stu-id="3bab0-126">tables</span></span>|<span data-ttu-id="3bab0-127">Colección [Table](table.md)</span><span class="sxs-lookup"><span data-stu-id="3bab0-127">[Table](table.md) collection</span></span>|<span data-ttu-id="3bab0-p102">Representa una colección de tablas asociadas con el libro. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3bab0-p102">Represents a collection of tables associated with the workbook. Read-only.</span></span>|
|<span data-ttu-id="3bab0-130">worksheets</span><span class="sxs-lookup"><span data-stu-id="3bab0-130">worksheets</span></span>|<span data-ttu-id="3bab0-131">Colección [Worksheet](worksheet.md)</span><span class="sxs-lookup"><span data-stu-id="3bab0-131">[Worksheet](worksheet.md) collection</span></span>|<span data-ttu-id="3bab0-p103">Representa una colección de hojas de cálculo asociadas con el libro. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3bab0-p103">Represents a collection of worksheets associated with the workbook. Read-only.</span></span>|

## <a name="functions"></a><span data-ttu-id="3bab0-134">Funciones</span><span class="sxs-lookup"><span data-stu-id="3bab0-134">Functions</span></span>

<span data-ttu-id="3bab0-135">[Funciones de Excel](#functions): Para invocar una función de libro, use la sintaxis `POST /workbook/functions/{function-name}` y proporcione los argumentos de la función en el cuerpo mediante un objeto JSON.</span><span class="sxs-lookup"><span data-stu-id="3bab0-135">[Excel functions](#functions): Invoke a workbook function using the syntax `POST /workbook/functions/{function-name}` and providing the function argument(s) in the body using a JSON object.</span></span> <span data-ttu-id="3bab0-136">Las cadenas `value` y `error` resultantes de la función se devuelven en el objeto de resultado de la función.</span><span class="sxs-lookup"><span data-stu-id="3bab0-136">The function's resulting `value` and any `error` strings are returned in the function result object.</span></span> <span data-ttu-id="3bab0-137">El valor `error` de `null` indica que la función se ha ejecutado correctamente.</span><span class="sxs-lookup"><span data-stu-id="3bab0-137">The `error` value of `null` indicates successful execution of the function.</span></span> 

<span data-ttu-id="3bab0-138">La lista completa de funciones admitidas se encuentra [aquí](https://support.office.com/es-ES/article/Excel-functions-alphabetical-b3944572-255d-4efb-bb96-c6d90033e188).</span><span class="sxs-lookup"><span data-stu-id="3bab0-138">The complete list of supported functions are listed [here](https://support.office.com/es-ES/article/Excel-functions-alphabetical-b3944572-255d-4efb-bb96-c6d90033e188).</span></span> <span data-ttu-id="3bab0-139">Consulte la firma de la función para obtener tipos de datos y nombres de parámetros específicos.</span><span class="sxs-lookup"><span data-stu-id="3bab0-139">Refer to the function signature for specific parameter names and data types.</span></span>

<span data-ttu-id="3bab0-140">_Notas importantes:_</span><span class="sxs-lookup"><span data-stu-id="3bab0-140">_Important notes:_</span></span> 
* <span data-ttu-id="3bab0-141">El parámetro de entrada de intervalo se suministra mediante un objeto range en lugar de la cadena de dirección de intervalo.</span><span class="sxs-lookup"><span data-stu-id="3bab0-141">The range input parameter is supplied using a range object instead of the range address string.</span></span>  
* <span data-ttu-id="3bab0-142">El parámetro de índice es “1 indexado”, a diferencia del “índice 0” usado en la mayoría de las API.</span><span class="sxs-lookup"><span data-stu-id="3bab0-142">The index parameter is 1-indexed unlike the 0-index used in most of the APIs.</span></span> 

<span data-ttu-id="3bab0-143">Ejemplo: **BUSCARV**</span><span class="sxs-lookup"><span data-stu-id="3bab0-143">Example: **vlookup**</span></span>

<span data-ttu-id="3bab0-144">En una hoja de cálculo de Excel, la función `vlookup` admite estos argumentos:</span><span class="sxs-lookup"><span data-stu-id="3bab0-144">In an Excel spreadsheet, the `vlookup` function takes the following arguments:</span></span>

1. <span data-ttu-id="3bab0-145">El valor que quiere buscar, también llamado el valor de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="3bab0-145">The value you want to look up, also called the lookup value.</span></span>
2. <span data-ttu-id="3bab0-146">El rango donde se encuentra el valor de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="3bab0-146">The range where the lookup value is located.</span></span> <span data-ttu-id="3bab0-147">Recuerde que el valor de búsqueda siempre tiene que estar en la primera columna del rango para que BUSCARV funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="3bab0-147">Remember that the lookup value should always be in the first column in the range for VLOOKUP to work correctly.</span></span> <span data-ttu-id="3bab0-148">Por ejemplo, si el valor de búsqueda se encuentra en la celda C2, el rango tiene que empezar con C.</span><span class="sxs-lookup"><span data-stu-id="3bab0-148">For example, if your lookup value is in cell C2 then your range should start with C.</span></span>
3. <span data-ttu-id="3bab0-149">El número de columna en el rango que contiene el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="3bab0-149">The column number in the range that contains the return value.</span></span> <span data-ttu-id="3bab0-150">Por ejemplo, si especifica B2:D11 como el rango, B será la primera columna, C la segunda, etc.</span><span class="sxs-lookup"><span data-stu-id="3bab0-150">For example, if you specify B2: D11 as the range, you should count B as the first column, C as the second, and so on.</span></span>
4. <span data-ttu-id="3bab0-151">De forma opcional, puede especificar VERDADERO si quiere obtener una coincidencia aproximada, o bien FALSO si quiere obtener una coincidencia exacta del valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="3bab0-151">Optionally, you can specify TRUE if you want an approximate match or FALSE if you want an exact match of the return value.</span></span> <span data-ttu-id="3bab0-152">Si no especifica nada, el valor predeterminado será siempre VERDADERO o coincidencia aproximada.</span><span class="sxs-lookup"><span data-stu-id="3bab0-152">If you don't specify anything, the default value will always be TRUE or approximate match.</span></span>

<span data-ttu-id="3bab0-153">Dentro de una celda, la función `vlookup` es similar a esta:</span><span class="sxs-lookup"><span data-stu-id="3bab0-153">Inside a cell, the `vlookup` function looks like this:</span></span> 

<span data-ttu-id="3bab0-154">= BUSCARV(valor de búsqueda, rango que contiene el valor de búsqueda, el número de columna en el rango que contiene el valor devuelto, de forma opcional, especifique VERDADERO para obtener una coincidencia aproximada o FALSO para una coincidencia exacta)</span><span class="sxs-lookup"><span data-stu-id="3bab0-154">=VLOOKUP(lookup value, range containing the lookup value, the column number in the range containing the return value, optionally specify TRUE for approximate match or FALSE for an exact match)</span></span>

<span data-ttu-id="3bab0-155">(Vea la documentación de la [Función de Excel BUSCARV](https://support.office.com/es-ES/article/VLOOKUP-function-0bbc8083-26fe-4963-8ab8-93a18ad188a1)).</span><span class="sxs-lookup"><span data-stu-id="3bab0-155">(See the documentation for the [VLOOKUP Excel function](https://support.office.com/es-ES/article/VLOOKUP-function-0bbc8083-26fe-4963-8ab8-93a18ad188a1).)</span></span>

<span data-ttu-id="3bab0-156">En el ejemplo siguiente, se muestra cómo realizar una llamada a la función `vlookup` y pasar estos parámetros con la API de REST de Excel.</span><span class="sxs-lookup"><span data-stu-id="3bab0-156">The example below shows how to call the `vlookup` function and pass these parameters with the Excel REST API.</span></span>

<span data-ttu-id="3bab0-157">Solicitud:</span><span class="sxs-lookup"><span data-stu-id="3bab0-157">Request:</span></span> 

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

<span data-ttu-id="3bab0-158">Respuesta:</span><span class="sxs-lookup"><span data-stu-id="3bab0-158">Response:</span></span>

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

<span data-ttu-id="3bab0-159">Ejemplo: `median`</span><span class="sxs-lookup"><span data-stu-id="3bab0-159">Example: `median`</span></span>

<span data-ttu-id="3bab0-160">En una hoja de cálculo de Excel, la función `median` admite una matriz de uno o más rangos de entrada.</span><span class="sxs-lookup"><span data-stu-id="3bab0-160">In an Excel spreadsheet, the `median` function takes an array of one or more input ranges.</span></span>

<span data-ttu-id="3bab0-161">Dentro de una celda, la función `median` es similar a este ejemplo:</span><span class="sxs-lookup"><span data-stu-id="3bab0-161">Inside a cell, the `median` function looks like this example:</span></span>

<span data-ttu-id="3bab0-162">=MEDIANA(A2:A6)</span><span class="sxs-lookup"><span data-stu-id="3bab0-162">=MEDIAN(A2:A6)</span></span>

<span data-ttu-id="3bab0-163">(Vea la documentación de la [Función de Excel MEDIANA](https://support.office.com/es-ES/article/MEDIAN-function-d0916313-4753-414c-8537-ce85bdd967d2)).</span><span class="sxs-lookup"><span data-stu-id="3bab0-163">(See the documentation for the [MEDIAN Excel function](https://support.office.com/es-ES/article/MEDIAN-function-d0916313-4753-414c-8537-ce85bdd967d2).)</span></span>

<span data-ttu-id="3bab0-164">En el ejemplo siguiente, se muestra cómo realizar una llamada a la función `median` y uno o más rangos de entrada con la API de REST de Excel.</span><span class="sxs-lookup"><span data-stu-id="3bab0-164">The example below shows how to call the `median` function and one or more input ranges with the Excel REST API.</span></span> 

<span data-ttu-id="3bab0-165">Solicitud:</span><span class="sxs-lookup"><span data-stu-id="3bab0-165">Request:</span></span> 

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

<span data-ttu-id="3bab0-166">Respuesta:</span><span class="sxs-lookup"><span data-stu-id="3bab0-166">Response:</span></span>

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
