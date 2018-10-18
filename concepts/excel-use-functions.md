# <a name="use-workbook-functions-in-excel-with-microsoft-graph"></a><span data-ttu-id="e6e03-101">Usar funciones de libro en Excel con Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="e6e03-101">Use workbook functions in Excel with Microsoft Graph</span></span>

<span data-ttu-id="e6e03-102">Puede invocar cualquier función de libro con la sintaxis siguiente: `POST /workbook/functions/{function-name}`.</span><span class="sxs-lookup"><span data-stu-id="e6e03-102">You can invoke any workbook function by using the following syntax: `POST /workbook/functions/{function-name}`.</span></span> <span data-ttu-id="e6e03-103">Especifique los argumentos de la función en el cuerpo con un objeto JSON.</span><span class="sxs-lookup"><span data-stu-id="e6e03-103">You provide the function argument(s) in the body using a JSON object.</span></span> <span data-ttu-id="e6e03-104">Las cadenas `value` y `error` resultantes de la función se devuelven en el objeto de resultado de la función.</span><span class="sxs-lookup"><span data-stu-id="e6e03-104">The function's resulting `value` and any `error` strings are returned in the function result object.</span></span> <span data-ttu-id="e6e03-105">El valor `error` de `null` indica que la función se ha ejecutado correctamente.</span><span class="sxs-lookup"><span data-stu-id="e6e03-105">The `error` value of `null` indicates successful execution of the function.</span></span>

<span data-ttu-id="e6e03-p102">La lista completa de funciones admitidas se encuentra [aquí](https://support.office.com/en-us/article/Excel-functions-alphabetical-b3944572-255d-4efb-bb96-c6d90033e188). Consulte la firma de la función para obtener tipos de datos y nombres de parámetros específicos.</span><span class="sxs-lookup"><span data-stu-id="e6e03-p102">The complete list of supported functions are listed [here](https://support.office.com/en-us/article/Excel-functions-alphabetical-b3944572-255d-4efb-bb96-c6d90033e188). Refer to the function signature for specific parameter names and data types.</span></span>

<span data-ttu-id="e6e03-108">_Notas importantes:_</span><span class="sxs-lookup"><span data-stu-id="e6e03-108">_Important notes:_</span></span>
* <span data-ttu-id="e6e03-109">El parámetro de entrada de intervalo se suministra mediante un objeto range en lugar de la cadena de dirección de intervalo.</span><span class="sxs-lookup"><span data-stu-id="e6e03-109">The range input parameter is supplied using a range object instead of the range address string.</span></span>  
* <span data-ttu-id="e6e03-110">El parámetro de índice es “1 indexado”, a diferencia del “índice 0” usado en la mayoría de las API.</span><span class="sxs-lookup"><span data-stu-id="e6e03-110">The index parameter is 1-indexed unlike the 0-index used in most of the APIs.</span></span>

<span data-ttu-id="e6e03-111">Ejemplo: **BUSCARV**</span><span class="sxs-lookup"><span data-stu-id="e6e03-111">Example: **vlookup**</span></span>

<span data-ttu-id="e6e03-112">En una hoja de cálculo de Excel, la función `vlookup` admite estos argumentos:</span><span class="sxs-lookup"><span data-stu-id="e6e03-112">In an Excel spreadsheet, the `vlookup` function takes the following arguments:</span></span>

1. <span data-ttu-id="e6e03-113">**valor_buscado** (obligatorio) El valor que quiere buscar.</span><span class="sxs-lookup"><span data-stu-id="e6e03-113">**lookup_value** (required) The value you want to look up.</span></span>
2. <span data-ttu-id="e6e03-114">**matriz_buscar_en** (obligatorio) El rango de celdas donde se encuentra el valor de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="e6e03-114">**table_array** (required) The range of cells where the lookup value is located.</span></span> <span data-ttu-id="e6e03-115">Recuerde que el valor de búsqueda siempre tiene que estar en la primera columna del rango para que BUSCARV funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="e6e03-115">Remember that the lookup value should always be in the first column in the range for VLOOKUP to work correctly.</span></span> <span data-ttu-id="e6e03-116">Por ejemplo, si el valor de búsqueda se encuentra en la celda C2, el rango tiene que empezar con C.</span><span class="sxs-lookup"><span data-stu-id="e6e03-116">For example, if your lookup value is in cell C2 then your range should start with C.</span></span>
3. <span data-ttu-id="e6e03-117">**indicador_columnas** (obligatorio) El número de columna en el rango que contiene el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="e6e03-117">**col_index_num** (required) The column number in the range that contains the return value.</span></span> <span data-ttu-id="e6e03-118">Por ejemplo, si especifica B2:D11 como el rango, B será la primera columna, C la segunda, etc.</span><span class="sxs-lookup"><span data-stu-id="e6e03-118">For example, if you specify B2: D11 as the range, you should count B as the first column, C as the second, and so on.</span></span>
4. <span data-ttu-id="e6e03-119">**búsqueda_en_rango** (opcional) El valor lógico que especifica si quiere usar **BUSCARV** para encontrar una coincidencia exacta o una coincidencia aproximada.</span><span class="sxs-lookup"><span data-stu-id="e6e03-119">**range_lookup** (optional) The logical value that specifies whether you want **VLOOKUP** to find an approximate or an exact match.</span></span> <span data-ttu-id="e6e03-120">De forma opcional, puede especificar **VERDADERO** si quiere obtener una coincidencia aproximada, o bien **FALSO** si quiere obtener una coincidencia exacta del valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="e6e03-120">Specify **TRUE** if you want an approximate match or **FALSE** if you want an exact match of the return value.</span></span> <span data-ttu-id="e6e03-121">Si no especifica nada, el valor predeterminado será siempre VERDADERO o coincidencia aproximada.</span><span class="sxs-lookup"><span data-stu-id="e6e03-121">If you don't specify anything, the default value will always be TRUE or approximate match.</span></span>

<span data-ttu-id="e6e03-122">Dentro de una celda, la función `vlookup` es similar a esta:</span><span class="sxs-lookup"><span data-stu-id="e6e03-122">Inside a cell, the `vlookup` function looks like this:</span></span>

<span data-ttu-id="e6e03-123">= BUSCARV(valor de búsqueda, rango que contiene el valor de búsqueda, el número de columna en el rango que contiene el valor devuelto, de forma opcional, especifique VERDADERO para obtener una coincidencia aproximada o FALSO para una coincidencia exacta)</span><span class="sxs-lookup"><span data-stu-id="e6e03-123">=VLOOKUP(lookup value, range containing the lookup value, the column number in the range containing the return value, optionally specify TRUE for approximate match or FALSE for an exact match)</span></span>

<span data-ttu-id="e6e03-124">(Vea la documentación de la [Función de Excel BUSCARV](https://support.office.com/en-us/article/VLOOKUP-function-0bbc8083-26fe-4963-8ab8-93a18ad188a1)).</span><span class="sxs-lookup"><span data-stu-id="e6e03-124">(See the documentation for the [VLOOKUP Excel function](https://support.office.com/en-us/article/VLOOKUP-function-0bbc8083-26fe-4963-8ab8-93a18ad188a1).)</span></span>


##### <a name="request"></a><span data-ttu-id="e6e03-125">Solicitud:</span><span class="sxs-lookup"><span data-stu-id="e6e03-125">Request:</span></span>
<span data-ttu-id="e6e03-126">En el ejemplo siguiente, se muestra cómo realizar una llamada a la función `vlookup` y pasar estos parámetros con la API de REST de Excel.</span><span class="sxs-lookup"><span data-stu-id="e6e03-126">The following example shows how to call the `vlookup` function and pass these parameters with the Excel REST API.</span></span>

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

##### <a name="response"></a><span data-ttu-id="e6e03-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e6e03-127">Response</span></span>

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

<span data-ttu-id="e6e03-128">Ejemplo: `median`</span><span class="sxs-lookup"><span data-stu-id="e6e03-128">Example: `median`</span></span>

<span data-ttu-id="e6e03-129">En una hoja de cálculo de Excel, la función `median` admite una matriz de uno o más rangos de entrada.</span><span class="sxs-lookup"><span data-stu-id="e6e03-129">In an Excel spreadsheet, the `median` function takes an array of one or more input ranges.</span></span>

<span data-ttu-id="e6e03-130">Dentro de una celda, la función `median` es similar a este ejemplo:</span><span class="sxs-lookup"><span data-stu-id="e6e03-130">Inside a cell, the `median` function looks like this example:</span></span>

<span data-ttu-id="e6e03-131">=MEDIANA(A2:A6)</span><span class="sxs-lookup"><span data-stu-id="e6e03-131">=MEDIAN(A2:A6)</span></span>

<span data-ttu-id="e6e03-132">(Vea la documentación de la [Función de Excel MEDIANA](https://support.office.com/en-us/article/MEDIAN-function-d0916313-4753-414c-8537-ce85bdd967d2)).</span><span class="sxs-lookup"><span data-stu-id="e6e03-132">(See the documentation for the [MEDIAN Excel function](https://support.office.com/en-us/article/MEDIAN-function-d0916313-4753-414c-8537-ce85bdd967d2).)</span></span>

##### <a name="request"></a><span data-ttu-id="e6e03-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e6e03-133">Request</span></span>
<span data-ttu-id="e6e03-134">En el ejemplo siguiente, se muestra cómo realizar una llamada a la función `median` y uno o más rangos de entrada con la API de REST de Excel.</span><span class="sxs-lookup"><span data-stu-id="e6e03-134">The following example shows how to call the `median` function and one or more input ranges with the Excel REST API.</span></span>

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

##### <a name="response"></a><span data-ttu-id="e6e03-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e6e03-135">Response</span></span>

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

## <a name="see-also"></a><span data-ttu-id="e6e03-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6e03-136">See also</span></span>
* [<span data-ttu-id="e6e03-137">Administrar sesiones en Excel con Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="e6e03-137">Manage sessions in Excel with Microsoft Graph</span></span>](excel-manage-sessions.md)
* [<span data-ttu-id="e6e03-138">Escribir en un libro de Excel con Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="e6e03-138">Write to an Excel workbook using Microsoft Graph</span></span>](excel-write-to-workbook.md)
* [<span data-ttu-id="e6e03-139">Actualizar el formato de un rango en Excel con Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="e6e03-139">Update a range’s format in Excel with Microsoft Graph</span></span>](excel-update-range-format.md)
* [<span data-ttu-id="e6e03-140">Mostrar una imagen de gráfico de Excel con Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="e6e03-140">Display a chart image in Excel with Microsoft Graph</span></span>](excel-display-chart-image.md)
* [<span data-ttu-id="e6e03-141">Usar la API de REST de Excel</span><span class="sxs-lookup"><span data-stu-id="e6e03-141">Use the Excel REST API</span></span>](../api-reference/v1.0/resources/excel.md)
