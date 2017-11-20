# <a name="rangebordercollection-itemat"></a><span data-ttu-id="d8f58-101">RangeBorderCollection: ItemAt</span><span class="sxs-lookup"><span data-stu-id="d8f58-101">RangeBorderCollection: ItemAt</span></span>

<span data-ttu-id="d8f58-102">Obtiene un objeto de borde mediante su índice.</span><span class="sxs-lookup"><span data-stu-id="d8f58-102">Gets a border object using its index</span></span>
## <a name="permissions"></a><span data-ttu-id="d8f58-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="d8f58-103">Permissions</span></span>
<span data-ttu-id="d8f58-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="d8f58-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="d8f58-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d8f58-106">Permission type</span></span>      | <span data-ttu-id="d8f58-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d8f58-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d8f58-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d8f58-108">Delegated (work or school account)</span></span> | <span data-ttu-id="d8f58-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d8f58-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="d8f58-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d8f58-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d8f58-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d8f58-111">Not supported.</span></span>    |
|<span data-ttu-id="d8f58-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d8f58-112">Application</span></span> | <span data-ttu-id="d8f58-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d8f58-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="d8f58-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d8f58-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names(<name>)/range/format/borders/ItemAt
POST /workbook/worksheets/{id|name}/range(address='<address>')/format/borders/ItemAt
POST /workbook/tables/{id|name}/columns/{id|name}/range/format/borders/ItemAt

```
## <a name="request-headers"></a><span data-ttu-id="d8f58-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d8f58-115">Request headers</span></span>
| <span data-ttu-id="d8f58-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="d8f58-116">Name</span></span>       | <span data-ttu-id="d8f58-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="d8f58-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="d8f58-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="d8f58-118">Authorization</span></span>  | <span data-ttu-id="d8f58-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d8f58-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="d8f58-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="d8f58-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="d8f58-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="d8f58-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="d8f58-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d8f58-124">Request body</span></span>
<span data-ttu-id="d8f58-125">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="d8f58-125">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="d8f58-126">Parámetro</span><span class="sxs-lookup"><span data-stu-id="d8f58-126">Parameter</span></span>    | <span data-ttu-id="d8f58-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="d8f58-127">Type</span></span>   |<span data-ttu-id="d8f58-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="d8f58-128">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d8f58-129">index</span><span class="sxs-lookup"><span data-stu-id="d8f58-129">index</span></span>|<span data-ttu-id="d8f58-130">number</span><span class="sxs-lookup"><span data-stu-id="d8f58-130">number</span></span>|<span data-ttu-id="d8f58-p104">Valor de índice del objeto que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="d8f58-p104">Index value of the object to be retrieved. Zero-indexed.</span></span>|

## <a name="response"></a><span data-ttu-id="d8f58-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d8f58-133">Response</span></span>

<span data-ttu-id="d8f58-134">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [RangeBorder](../resources/rangeborder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d8f58-134">If successful, this method returns `200 OK` response code and [RangeBorder](../resources/rangeborder.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d8f58-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d8f58-135">Example</span></span>
<span data-ttu-id="d8f58-136">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="d8f58-136">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="d8f58-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d8f58-137">Request</span></span>
<span data-ttu-id="d8f58-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d8f58-138">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "rangebordercollection_itemat"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/range/format/borders/ItemAt
Content-type: application/json
Content-length: 20

{
  "index": {
  }
}
```

##### <a name="response"></a><span data-ttu-id="d8f58-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d8f58-139">Response</span></span>
<span data-ttu-id="d8f58-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d8f58-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.rangeBorder"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 136

{
  "id": "id-value",
  "color": "color-value",
  "style": "style-value",
  "sideIndex": "sideIndex-value",
  "weight": "weight-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "RangeBorderCollection: ItemAt",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->