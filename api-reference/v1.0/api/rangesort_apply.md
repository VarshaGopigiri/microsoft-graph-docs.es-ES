# <a name="rangesort-apply"></a><span data-ttu-id="d3439-101">RangeSort: apply</span><span class="sxs-lookup"><span data-stu-id="d3439-101">RangeSort: apply</span></span>

<span data-ttu-id="d3439-102">Realiza una operación de ordenación.</span><span class="sxs-lookup"><span data-stu-id="d3439-102">Perform a sort operation.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d3439-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d3439-103">Prerequisites</span></span>
<span data-ttu-id="d3439-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="d3439-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="d3439-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d3439-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="d3439-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d3439-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names(<name>)/range/sort/apply
POST /workbook/worksheets/{id|name}/range(<address>)/sort/apply
POST /workbook/tables/{id|name}/columns/{id|name}/range/sort/apply

```
## <a name="request-headers"></a><span data-ttu-id="d3439-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d3439-107">Request headers</span></span>
| <span data-ttu-id="d3439-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="d3439-108">Name</span></span>       | <span data-ttu-id="d3439-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3439-109">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="d3439-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="d3439-110">Authorization</span></span>  | <span data-ttu-id="d3439-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d3439-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="d3439-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d3439-113">Request body</span></span>
<span data-ttu-id="d3439-114">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="d3439-114">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="d3439-115">Parámetro</span><span class="sxs-lookup"><span data-stu-id="d3439-115">Parameter</span></span>    | <span data-ttu-id="d3439-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="d3439-116">Type</span></span>   |<span data-ttu-id="d3439-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3439-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d3439-118">fields</span><span class="sxs-lookup"><span data-stu-id="d3439-118">fields</span></span>|<span data-ttu-id="d3439-119">SortField</span><span class="sxs-lookup"><span data-stu-id="d3439-119">SortField</span></span>|<span data-ttu-id="d3439-120">La lista de condiciones por las que realizar la ordenación.</span><span class="sxs-lookup"><span data-stu-id="d3439-120">The list of conditions to sort on.</span></span>|
|<span data-ttu-id="d3439-121">matchCase</span><span class="sxs-lookup"><span data-stu-id="d3439-121">matchCase</span></span>|<span data-ttu-id="d3439-122">boolean</span><span class="sxs-lookup"><span data-stu-id="d3439-122">boolean</span></span>|<span data-ttu-id="d3439-p102">Opcional. Indica si la ordenación de cadenas distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d3439-p102">Optional. Whether to have the casing impact string ordering.</span></span>|
|<span data-ttu-id="d3439-125">hasHeaders</span><span class="sxs-lookup"><span data-stu-id="d3439-125">hasHeaders</span></span>|<span data-ttu-id="d3439-126">boolean</span><span class="sxs-lookup"><span data-stu-id="d3439-126">boolean</span></span>|<span data-ttu-id="d3439-p103">Opcional. Si el rango tiene un encabezado.</span><span class="sxs-lookup"><span data-stu-id="d3439-p103">Optional. Whether the range has a header.</span></span>|
|<span data-ttu-id="d3439-129">orientation</span><span class="sxs-lookup"><span data-stu-id="d3439-129">orientation</span></span>|<span data-ttu-id="d3439-130">string</span><span class="sxs-lookup"><span data-stu-id="d3439-130">string</span></span>|<span data-ttu-id="d3439-p104">Opcional. Indica si la operación ordena filas o columnas.  Valores posibles: `Rows`, `Columns`.</span><span class="sxs-lookup"><span data-stu-id="d3439-p104">Optional. Whether the operation is sorting rows or columns.  Possible values are: `Rows`, `Columns`.</span></span>|
|<span data-ttu-id="d3439-134">method</span><span class="sxs-lookup"><span data-stu-id="d3439-134">method</span></span>|<span data-ttu-id="d3439-135">string</span><span class="sxs-lookup"><span data-stu-id="d3439-135">string</span></span>|<span data-ttu-id="d3439-p105">Opcional. Método de ordenación que se usa para los caracteres chinos.  Valores posibles: `PinYin`, `StrokeCount`.</span><span class="sxs-lookup"><span data-stu-id="d3439-p105">Optional. The ordering method used for Chinese characters.  Possible values are: `PinYin`, `StrokeCount`.</span></span>|

## <a name="response"></a><span data-ttu-id="d3439-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d3439-139">Response</span></span>

<span data-ttu-id="d3439-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d3439-p106">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d3439-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d3439-142">Example</span></span>
<span data-ttu-id="d3439-143">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="d3439-143">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="d3439-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d3439-144">Request</span></span>
<span data-ttu-id="d3439-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d3439-145">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "rangesort_apply"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/range/sort/apply
Content-type: application/json
Content-length: 358

{
  "fields": [
    {
      "key": 99,
      "sortOn": "sortOn-value",
      "ascending": true,
      "color": "color-value",
      "dataOption": "dataOption-value",
      "icon": {
        "set": "set-value",
        "index": 99
      }
    }
  ],
  "matchCase": true,
  "hasHeaders": true,
  "orientation": "orientation-value",
  "method": "method-value"
}
```

##### <a name="response"></a><span data-ttu-id="d3439-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d3439-146">Response</span></span>
<span data-ttu-id="d3439-147">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d3439-147">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.none"
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "RangeSort: apply",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->