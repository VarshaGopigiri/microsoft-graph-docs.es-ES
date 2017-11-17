# <a name="rangesort-apply"></a><span data-ttu-id="f0050-101">RangeSort: apply</span><span class="sxs-lookup"><span data-stu-id="f0050-101">RangeSort: apply</span></span>

<span data-ttu-id="f0050-102">Realizar una operación de ordenación.</span><span class="sxs-lookup"><span data-stu-id="f0050-102">Perform a sort operation.</span></span>
## <a name="permissions"></a><span data-ttu-id="f0050-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="f0050-103">Permissions</span></span>
<span data-ttu-id="f0050-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="f0050-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="f0050-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f0050-106">Permission type</span></span>      | <span data-ttu-id="f0050-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f0050-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f0050-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f0050-108">Delegated (work or school account)</span></span> | <span data-ttu-id="f0050-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f0050-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="f0050-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f0050-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f0050-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f0050-111">Not supported.</span></span>    |
|<span data-ttu-id="f0050-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f0050-112">Application</span></span> | <span data-ttu-id="f0050-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f0050-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="f0050-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f0050-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names(<name>)/range/sort/apply
POST /workbook/worksheets/{id|name}/range(address='<address>')/sort/apply
POST /workbook/tables/{id|name}/columns/{id|name}/range/sort/apply

```
## <a name="request-headers"></a><span data-ttu-id="f0050-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f0050-115">Request headers</span></span>
| <span data-ttu-id="f0050-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="f0050-116">Name</span></span>       | <span data-ttu-id="f0050-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="f0050-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="f0050-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="f0050-118">Authorization</span></span>  | <span data-ttu-id="f0050-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f0050-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="f0050-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f0050-121">Request body</span></span>
<span data-ttu-id="f0050-122">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="f0050-122">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="f0050-123">Parámetro</span><span class="sxs-lookup"><span data-stu-id="f0050-123">Parameter</span></span>    | <span data-ttu-id="f0050-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="f0050-124">Type</span></span>   |<span data-ttu-id="f0050-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="f0050-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f0050-126">fields</span><span class="sxs-lookup"><span data-stu-id="f0050-126">fields</span></span>|<span data-ttu-id="f0050-127">SortField</span><span class="sxs-lookup"><span data-stu-id="f0050-127">SortField</span></span>|<span data-ttu-id="f0050-128">La lista de condiciones por las que realizar la ordenación.</span><span class="sxs-lookup"><span data-stu-id="f0050-128">The list of conditions to sort on.</span></span>|
|<span data-ttu-id="f0050-129">matchCase</span><span class="sxs-lookup"><span data-stu-id="f0050-129">matchCase</span></span>|<span data-ttu-id="f0050-130">boolean</span><span class="sxs-lookup"><span data-stu-id="f0050-130">boolean</span></span>|<span data-ttu-id="f0050-p103">Opcional. Indica si la ordenación de cadenas distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f0050-p103">Optional. Whether to have the casing impact string ordering.</span></span>|
|<span data-ttu-id="f0050-133">hasHeaders</span><span class="sxs-lookup"><span data-stu-id="f0050-133">hasHeaders</span></span>|<span data-ttu-id="f0050-134">boolean</span><span class="sxs-lookup"><span data-stu-id="f0050-134">boolean</span></span>|<span data-ttu-id="f0050-p104">Opcional. Si el rango tiene un encabezado.</span><span class="sxs-lookup"><span data-stu-id="f0050-p104">Optional. Whether the range has a header.</span></span>|
|<span data-ttu-id="f0050-137">orientation</span><span class="sxs-lookup"><span data-stu-id="f0050-137">orientation</span></span>|<span data-ttu-id="f0050-138">string</span><span class="sxs-lookup"><span data-stu-id="f0050-138">string</span></span>|<span data-ttu-id="f0050-p105">Opcional. Indica si la operación ordena filas o columnas.  Valores posibles: `Rows`, `Columns`.</span><span class="sxs-lookup"><span data-stu-id="f0050-p105">Optional. Whether the operation is sorting rows or columns.  Possible values are: `Rows`, `Columns`.</span></span>|
|<span data-ttu-id="f0050-142">method</span><span class="sxs-lookup"><span data-stu-id="f0050-142">method</span></span>|<span data-ttu-id="f0050-143">string</span><span class="sxs-lookup"><span data-stu-id="f0050-143">string</span></span>|<span data-ttu-id="f0050-p106">Opcional. Método de ordenación que se usa para los caracteres chinos.  Valores posibles: `PinYin`, `StrokeCount`.</span><span class="sxs-lookup"><span data-stu-id="f0050-p106">Optional. The ordering method used for Chinese characters.  Possible values are: `PinYin`, `StrokeCount`.</span></span>|

## <a name="response"></a><span data-ttu-id="f0050-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f0050-147">Response</span></span>

<span data-ttu-id="f0050-p107">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f0050-p107">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f0050-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f0050-150">Example</span></span>
<span data-ttu-id="f0050-151">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="f0050-151">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="f0050-152">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f0050-152">Request</span></span>
<span data-ttu-id="f0050-153">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f0050-153">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="f0050-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f0050-154">Response</span></span>
<span data-ttu-id="f0050-155">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f0050-155">Here is an example of the response.</span></span> 
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