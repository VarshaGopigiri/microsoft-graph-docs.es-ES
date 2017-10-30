# <a name="range-delete"></a><span data-ttu-id="08a31-101">Range: delete</span><span class="sxs-lookup"><span data-stu-id="08a31-101">Range: delete</span></span>

<span data-ttu-id="08a31-102">Elimina las celdas asociadas al rango.</span><span class="sxs-lookup"><span data-stu-id="08a31-102">Deletes the cells associated with the range.</span></span>
## <a name="permissions"></a><span data-ttu-id="08a31-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="08a31-103">Permissions</span></span>
<span data-ttu-id="08a31-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="08a31-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="08a31-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="08a31-106">Permission type</span></span>      | <span data-ttu-id="08a31-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="08a31-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="08a31-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="08a31-108">Delegated (work or school account)</span></span> | <span data-ttu-id="08a31-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="08a31-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="08a31-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="08a31-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="08a31-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="08a31-111">Not supported.</span></span>    |
|<span data-ttu-id="08a31-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="08a31-112">Application</span></span> | <span data-ttu-id="08a31-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="08a31-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="08a31-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="08a31-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names(<name>)/range/delete
POST /workbook/worksheets/{id|name}/range(address='<address>')/delete
POST /workbook/tables/{id|name}/columns/{id|name}/range/delete

```
## <a name="request-headers"></a><span data-ttu-id="08a31-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="08a31-115">Request headers</span></span>
| <span data-ttu-id="08a31-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="08a31-116">Name</span></span>       | <span data-ttu-id="08a31-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="08a31-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="08a31-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="08a31-118">Authorization</span></span>  | <span data-ttu-id="08a31-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="08a31-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="08a31-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="08a31-121">Request body</span></span>
<span data-ttu-id="08a31-122">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="08a31-122">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="08a31-123">Parámetro</span><span class="sxs-lookup"><span data-stu-id="08a31-123">Parameter</span></span>    | <span data-ttu-id="08a31-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="08a31-124">Type</span></span>   |<span data-ttu-id="08a31-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="08a31-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="08a31-126">Shift</span><span class="sxs-lookup"><span data-stu-id="08a31-126">shift</span></span>|<span data-ttu-id="08a31-127">string</span><span class="sxs-lookup"><span data-stu-id="08a31-127">string</span></span>|<span data-ttu-id="08a31-p103">Especifica hacia dónde se desplazarán las celdas.  Valores posibles: `Up`, `Left`.</span><span class="sxs-lookup"><span data-stu-id="08a31-p103">Specifies which way to shift the cells.  Possible values are: `Up`, `Left`.</span></span>|

## <a name="response"></a><span data-ttu-id="08a31-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="08a31-130">Response</span></span>

<span data-ttu-id="08a31-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="08a31-p104">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="08a31-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="08a31-133">Example</span></span>
<span data-ttu-id="08a31-134">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="08a31-134">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="08a31-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="08a31-135">Request</span></span>
<span data-ttu-id="08a31-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="08a31-136">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="08a31-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="08a31-137">Response</span></span>
<span data-ttu-id="08a31-138">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="08a31-138">Here is an example of the response.</span></span> 
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