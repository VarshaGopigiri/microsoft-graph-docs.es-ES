# <a name="tablesort-apply"></a><span data-ttu-id="9ce91-101">TableSort: apply</span><span class="sxs-lookup"><span data-stu-id="9ce91-101">TableSort: apply</span></span>

<span data-ttu-id="9ce91-102">Realizar una operación de ordenación.</span><span class="sxs-lookup"><span data-stu-id="9ce91-102">Perform a sort operation.</span></span>
## <a name="permissions"></a><span data-ttu-id="9ce91-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="9ce91-103">Permissions</span></span>
<span data-ttu-id="9ce91-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="9ce91-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="9ce91-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9ce91-106">Permission type</span></span>      | <span data-ttu-id="9ce91-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9ce91-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9ce91-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9ce91-108">Delegated (work or school account)</span></span> | <span data-ttu-id="9ce91-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9ce91-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="9ce91-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9ce91-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9ce91-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9ce91-111">Not supported.</span></span>    |
|<span data-ttu-id="9ce91-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9ce91-112">Application</span></span> | <span data-ttu-id="9ce91-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9ce91-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="9ce91-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9ce91-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/sort/apply
POST /workbook/worksheets/{id|name}/tables/{id|name}/sort/apply

```
## <a name="request-headers"></a><span data-ttu-id="9ce91-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9ce91-115">Request headers</span></span>
| <span data-ttu-id="9ce91-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="9ce91-116">Name</span></span>       | <span data-ttu-id="9ce91-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="9ce91-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="9ce91-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="9ce91-118">Authorization</span></span>  | <span data-ttu-id="9ce91-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9ce91-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="9ce91-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="9ce91-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="9ce91-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="9ce91-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="9ce91-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9ce91-124">Request body</span></span>
<span data-ttu-id="9ce91-125">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="9ce91-125">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="9ce91-126">Parámetro</span><span class="sxs-lookup"><span data-stu-id="9ce91-126">Parameter</span></span>    | <span data-ttu-id="9ce91-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="9ce91-127">Type</span></span>   |<span data-ttu-id="9ce91-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="9ce91-128">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9ce91-129">fields</span><span class="sxs-lookup"><span data-stu-id="9ce91-129">fields</span></span>|<span data-ttu-id="9ce91-130">colección WorkbookSortField</span><span class="sxs-lookup"><span data-stu-id="9ce91-130">WorkbookSortField collection</span></span>|<span data-ttu-id="9ce91-131">La lista de condiciones por las que realizar la ordenación.</span><span class="sxs-lookup"><span data-stu-id="9ce91-131">The list of conditions to sort on.</span></span>|
|<span data-ttu-id="9ce91-132">matchCase</span><span class="sxs-lookup"><span data-stu-id="9ce91-132">matchCase</span></span>|<span data-ttu-id="9ce91-133">booleano</span><span class="sxs-lookup"><span data-stu-id="9ce91-133">boolean</span></span>|<span data-ttu-id="9ce91-p104">Opcional. Indica si la ordenación de cadenas distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="9ce91-p104">Optional. Whether to have the casing impact string ordering.</span></span>|
|<span data-ttu-id="9ce91-136">method</span><span class="sxs-lookup"><span data-stu-id="9ce91-136">method</span></span>|<span data-ttu-id="9ce91-137">cadena</span><span class="sxs-lookup"><span data-stu-id="9ce91-137">string</span></span>|<span data-ttu-id="9ce91-138">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9ce91-138">Optional.</span></span> <span data-ttu-id="9ce91-139">El método de ordenación que se utiliza para los caracteres chinos.</span><span class="sxs-lookup"><span data-stu-id="9ce91-139">Optional. The ordering method used for Chinese characters.  Possible values are: , .</span></span>  <span data-ttu-id="9ce91-140">Los valores posibles son: `PinYin` y `StrokeCount`.</span><span class="sxs-lookup"><span data-stu-id="9ce91-140">The possible values are:</span></span>|

## <a name="response"></a><span data-ttu-id="9ce91-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9ce91-141">Response</span></span>

<span data-ttu-id="9ce91-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9ce91-p106">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9ce91-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9ce91-144">Example</span></span>
<span data-ttu-id="9ce91-145">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="9ce91-145">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="9ce91-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9ce91-146">Request</span></span>
<span data-ttu-id="9ce91-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9ce91-147">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "tablesort_apply"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/sort/apply
Content-type: application/json
Content-length: 298

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
  "method": "method-value"
}
```

##### <a name="response"></a><span data-ttu-id="9ce91-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9ce91-148">Response</span></span>
<span data-ttu-id="9ce91-149">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9ce91-149">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "TableSort: apply",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->