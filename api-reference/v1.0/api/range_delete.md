# <a name="range-delete"></a><span data-ttu-id="6fd0e-101">Range: delete</span><span class="sxs-lookup"><span data-stu-id="6fd0e-101">Range: delete</span></span>

<span data-ttu-id="6fd0e-102">Elimina las celdas asociadas al rango.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-102">Deletes the cells associated with the range.</span></span>
## <a name="permissions"></a><span data-ttu-id="6fd0e-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="6fd0e-103">Permissions</span></span>
<span data-ttu-id="6fd0e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="6fd0e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="6fd0e-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6fd0e-106">Permission type</span></span>      | <span data-ttu-id="6fd0e-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6fd0e-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6fd0e-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6fd0e-108">Delegated (work or school account)</span></span> | <span data-ttu-id="6fd0e-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6fd0e-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="6fd0e-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6fd0e-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6fd0e-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-111">Not supported.</span></span>    |
|<span data-ttu-id="6fd0e-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6fd0e-112">Application</span></span> | <span data-ttu-id="6fd0e-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="6fd0e-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6fd0e-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names(<name>)/range/delete
POST /workbook/worksheets/{id|name}/range(address='<address>')/delete
POST /workbook/tables/{id|name}/columns/{id|name}/range/delete

```
## <a name="request-headers"></a><span data-ttu-id="6fd0e-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6fd0e-115">Request headers</span></span>
| <span data-ttu-id="6fd0e-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="6fd0e-116">Name</span></span>       | <span data-ttu-id="6fd0e-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="6fd0e-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="6fd0e-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="6fd0e-118">Authorization</span></span>  | <span data-ttu-id="6fd0e-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="6fd0e-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="6fd0e-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="6fd0e-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="6fd0e-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6fd0e-124">Request body</span></span>
<span data-ttu-id="6fd0e-125">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-125">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="6fd0e-126">Parámetro</span><span class="sxs-lookup"><span data-stu-id="6fd0e-126">Parameter</span></span>    | <span data-ttu-id="6fd0e-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="6fd0e-127">Type</span></span>   |<span data-ttu-id="6fd0e-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="6fd0e-128">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6fd0e-129">Shift</span><span class="sxs-lookup"><span data-stu-id="6fd0e-129">shift</span></span>|<span data-ttu-id="6fd0e-130">string</span><span class="sxs-lookup"><span data-stu-id="6fd0e-130">string</span></span>|<span data-ttu-id="6fd0e-p104">Especifica hacia dónde se desplazarán las celdas.  Valores posibles: `Up`, `Left`.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-p104">Specifies which way to shift the cells.  Possible values are: `Up`, `Left`.</span></span>|

## <a name="response"></a><span data-ttu-id="6fd0e-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6fd0e-133">Response</span></span>

<span data-ttu-id="6fd0e-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-p105">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6fd0e-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6fd0e-136">Example</span></span>
<span data-ttu-id="6fd0e-137">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-137">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="6fd0e-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6fd0e-138">Request</span></span>
<span data-ttu-id="6fd0e-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-139">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_delete"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/range/delete
Content-type: application/json
Content-length: 28

{
  "shift": "shift-value"
}
```

##### <a name="response"></a><span data-ttu-id="6fd0e-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6fd0e-140">Response</span></span>
<span data-ttu-id="6fd0e-141">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6fd0e-141">Here is an example of the response.</span></span> 
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
  "description": "Range: delete",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->