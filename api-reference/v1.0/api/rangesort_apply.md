# <a name="rangesort-apply"></a><span data-ttu-id="2bceb-101">RangeSort: apply</span><span class="sxs-lookup"><span data-stu-id="2bceb-101">RangeSort: apply</span></span>

<span data-ttu-id="2bceb-102">Realizar una operación de ordenación.</span><span class="sxs-lookup"><span data-stu-id="2bceb-102">Perform a sort operation.</span></span>
## <a name="permissions"></a><span data-ttu-id="2bceb-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="2bceb-103">Permissions</span></span>
<span data-ttu-id="2bceb-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="2bceb-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="2bceb-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2bceb-106">Permission type</span></span>      | <span data-ttu-id="2bceb-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2bceb-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2bceb-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2bceb-108">Delegated (work or school account)</span></span> | <span data-ttu-id="2bceb-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2bceb-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="2bceb-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2bceb-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2bceb-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2bceb-111">Not supported.</span></span>    |
|<span data-ttu-id="2bceb-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2bceb-112">Application</span></span> | <span data-ttu-id="2bceb-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2bceb-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="2bceb-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2bceb-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names(<name>)/range/sort/apply
POST /workbook/worksheets/{id|name}/range(address='<address>')/sort/apply
POST /workbook/tables/{id|name}/columns/{id|name}/range/sort/apply

```
## <a name="request-headers"></a><span data-ttu-id="2bceb-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2bceb-115">Request headers</span></span>
| <span data-ttu-id="2bceb-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="2bceb-116">Name</span></span>       | <span data-ttu-id="2bceb-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="2bceb-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="2bceb-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="2bceb-118">Authorization</span></span>  | <span data-ttu-id="2bceb-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2bceb-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="2bceb-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="2bceb-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="2bceb-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="2bceb-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="2bceb-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2bceb-124">Request body</span></span>
<span data-ttu-id="2bceb-125">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="2bceb-125">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="2bceb-126">Parámetro</span><span class="sxs-lookup"><span data-stu-id="2bceb-126">Parameter</span></span>    | <span data-ttu-id="2bceb-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="2bceb-127">Type</span></span>   |<span data-ttu-id="2bceb-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="2bceb-128">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2bceb-129">fields</span><span class="sxs-lookup"><span data-stu-id="2bceb-129">fields</span></span>|<span data-ttu-id="2bceb-130">SortField</span><span class="sxs-lookup"><span data-stu-id="2bceb-130">SortField</span></span>|<span data-ttu-id="2bceb-131">La lista de condiciones por las que realizar la ordenación.</span><span class="sxs-lookup"><span data-stu-id="2bceb-131">The list of conditions to sort on.</span></span>|
|<span data-ttu-id="2bceb-132">matchCase</span><span class="sxs-lookup"><span data-stu-id="2bceb-132">matchCase</span></span>|<span data-ttu-id="2bceb-133">boolean</span><span class="sxs-lookup"><span data-stu-id="2bceb-133">boolean</span></span>|<span data-ttu-id="2bceb-p104">Opcional. Indica si la ordenación de cadenas distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="2bceb-p104">Optional. Whether to have the casing impact string ordering.</span></span>|
|<span data-ttu-id="2bceb-136">hasHeaders</span><span class="sxs-lookup"><span data-stu-id="2bceb-136">hasHeaders</span></span>|<span data-ttu-id="2bceb-137">boolean</span><span class="sxs-lookup"><span data-stu-id="2bceb-137">boolean</span></span>|<span data-ttu-id="2bceb-p105">Opcional. Si el rango tiene un encabezado.</span><span class="sxs-lookup"><span data-stu-id="2bceb-p105">Optional. Whether the range has a header.</span></span>|
|<span data-ttu-id="2bceb-140">orientation</span><span class="sxs-lookup"><span data-stu-id="2bceb-140">orientation</span></span>|<span data-ttu-id="2bceb-141">string</span><span class="sxs-lookup"><span data-stu-id="2bceb-141">string</span></span>|<span data-ttu-id="2bceb-p106">Opcional. Indica si la operación ordena filas o columnas.  Valores posibles: `Rows`, `Columns`.</span><span class="sxs-lookup"><span data-stu-id="2bceb-p106">Optional. Whether the operation is sorting rows or columns.  Possible values are: `Rows`, `Columns`.</span></span>|
|<span data-ttu-id="2bceb-145">method</span><span class="sxs-lookup"><span data-stu-id="2bceb-145">method</span></span>|<span data-ttu-id="2bceb-146">string</span><span class="sxs-lookup"><span data-stu-id="2bceb-146">string</span></span>|<span data-ttu-id="2bceb-p107">Opcional. Método de ordenación que se usa para los caracteres chinos.  Valores posibles: `PinYin`, `StrokeCount`.</span><span class="sxs-lookup"><span data-stu-id="2bceb-p107">Optional. The ordering method used for Chinese characters.  Possible values are: `PinYin`, `StrokeCount`.</span></span>|

## <a name="response"></a><span data-ttu-id="2bceb-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2bceb-150">Response</span></span>

<span data-ttu-id="2bceb-p108">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2bceb-p108">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2bceb-153">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2bceb-153">Example</span></span>
<span data-ttu-id="2bceb-154">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="2bceb-154">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="2bceb-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2bceb-155">Request</span></span>
<span data-ttu-id="2bceb-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2bceb-156">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="2bceb-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2bceb-157">Response</span></span>
<span data-ttu-id="2bceb-158">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2bceb-158">Here is an example of the response.</span></span> 
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