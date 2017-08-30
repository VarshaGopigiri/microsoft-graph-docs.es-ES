# <a name="worksheetcollection-add"></a><span data-ttu-id="5946c-101">WorksheetCollection: add</span><span class="sxs-lookup"><span data-stu-id="5946c-101">WorksheetCollection: add</span></span>

<span data-ttu-id="5946c-p101">Agrega una nueva hoja al libro. La hoja de cálculo se agregará al final de las hojas de cálculo existentes. Si desea activar la hoja de cálculo recién agregada, llame en ella a ".activate().</span><span class="sxs-lookup"><span data-stu-id="5946c-p101">Adds a new worksheet to the workbook. The worksheet will be added at the end of existing worksheets. If you wish to activate the newly added worksheet, call ".activate() on it.</span></span>
## <a name="permissions"></a><span data-ttu-id="5946c-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="5946c-105">Permissions</span></span>
<span data-ttu-id="5946c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="5946c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="5946c-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5946c-108">Permission type</span></span>      | <span data-ttu-id="5946c-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5946c-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5946c-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5946c-110">Delegated (work or school account)</span></span> | <span data-ttu-id="5946c-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5946c-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="5946c-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5946c-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5946c-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5946c-113">Not supported.</span></span>    |
|<span data-ttu-id="5946c-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5946c-114">Application</span></span> | <span data-ttu-id="5946c-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5946c-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="5946c-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5946c-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/

```
## <a name="request-headers"></a><span data-ttu-id="5946c-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5946c-117">Request headers</span></span>
| <span data-ttu-id="5946c-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="5946c-118">Name</span></span>       | <span data-ttu-id="5946c-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="5946c-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="5946c-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="5946c-120">Authorization</span></span>  | <span data-ttu-id="5946c-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5946c-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="5946c-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5946c-123">Request body</span></span>
<span data-ttu-id="5946c-124">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="5946c-124">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="5946c-125">Parámetro</span><span class="sxs-lookup"><span data-stu-id="5946c-125">Parameter</span></span>    | <span data-ttu-id="5946c-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="5946c-126">Type</span></span>   |<span data-ttu-id="5946c-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="5946c-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5946c-128">name</span><span class="sxs-lookup"><span data-stu-id="5946c-128">name</span></span>|<span data-ttu-id="5946c-129">string</span><span class="sxs-lookup"><span data-stu-id="5946c-129">string</span></span>|<span data-ttu-id="5946c-p104">Opcional. Nombre de la hoja de cálculo que se va a agregar. Si se especifica, el nombre debe ser único. Si no se especifica, Excel determina el nombre de la nueva hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="5946c-p104">Optional. The name of the worksheet to be added. If specified, name should be unqiue. If not specified, Excel determines the name of the new worksheet.</span></span>|

## <a name="response"></a><span data-ttu-id="5946c-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5946c-134">Response</span></span>

<span data-ttu-id="5946c-135">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [Worksheet](../resources/worksheet.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5946c-135">If successful, this method returns `200, OK` response code and [Worksheet](../resources/worksheet.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5946c-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5946c-136">Example</span></span>
<span data-ttu-id="5946c-137">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="5946c-137">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="5946c-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5946c-138">Request</span></span>
<span data-ttu-id="5946c-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5946c-139">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "worksheetcollection_add"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/add
Content-type: application/json
Content-length: 26

{
  "name": "name-value"
}
```

##### <a name="response"></a><span data-ttu-id="5946c-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5946c-140">Response</span></span>
<span data-ttu-id="5946c-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5946c-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.worksheet"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 100

{
  "id": "id-value",
  "position": 99,
  "name": "name-value",
  "visibility": "visibility-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "WorksheetCollection: add",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->