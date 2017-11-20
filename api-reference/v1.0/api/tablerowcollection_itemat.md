# <a name="tablerowcollection-itemat"></a><span data-ttu-id="6aa3a-101">TableRowCollection: ItemAt</span><span class="sxs-lookup"><span data-stu-id="6aa3a-101">TableRowCollection: ItemAt</span></span>

<span data-ttu-id="6aa3a-102">Obtiene una fila en función de su posición en la colección.</span><span class="sxs-lookup"><span data-stu-id="6aa3a-102">Gets a row based on its position in the collection.</span></span>
## <a name="permissions"></a><span data-ttu-id="6aa3a-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="6aa3a-103">Permissions</span></span>
<span data-ttu-id="6aa3a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="6aa3a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="6aa3a-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6aa3a-106">Permission type</span></span>      | <span data-ttu-id="6aa3a-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6aa3a-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6aa3a-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6aa3a-108">Delegated (work or school account)</span></span> | <span data-ttu-id="6aa3a-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6aa3a-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="6aa3a-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6aa3a-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6aa3a-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6aa3a-111">Not supported.</span></span>    |
|<span data-ttu-id="6aa3a-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6aa3a-112">Application</span></span> | <span data-ttu-id="6aa3a-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6aa3a-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="6aa3a-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6aa3a-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/rows/ItemAt
POST /workbook/worksheets/{id|name}/tables/{id|name}/rows/ItemAt

```
## <a name="request-headers"></a><span data-ttu-id="6aa3a-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6aa3a-115">Request headers</span></span>
| <span data-ttu-id="6aa3a-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="6aa3a-116">Name</span></span>       | <span data-ttu-id="6aa3a-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="6aa3a-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="6aa3a-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="6aa3a-118">Authorization</span></span>  | <span data-ttu-id="6aa3a-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6aa3a-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="6aa3a-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="6aa3a-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="6aa3a-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="6aa3a-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="6aa3a-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6aa3a-124">Request body</span></span>
<span data-ttu-id="6aa3a-125">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="6aa3a-125">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="6aa3a-126">Parámetro</span><span class="sxs-lookup"><span data-stu-id="6aa3a-126">Parameter</span></span>    | <span data-ttu-id="6aa3a-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="6aa3a-127">Type</span></span>   |<span data-ttu-id="6aa3a-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="6aa3a-128">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6aa3a-129">index</span><span class="sxs-lookup"><span data-stu-id="6aa3a-129">index</span></span>|<span data-ttu-id="6aa3a-130">number</span><span class="sxs-lookup"><span data-stu-id="6aa3a-130">number</span></span>|<span data-ttu-id="6aa3a-p104">Valor de índice del objeto que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="6aa3a-p104">Index value of the object to be retrieved. Zero-indexed.</span></span>|

## <a name="response"></a><span data-ttu-id="6aa3a-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6aa3a-133">Response</span></span>

<span data-ttu-id="6aa3a-134">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [TableRow](../resources/tablerow.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6aa3a-134">If successful, this method returns `200 OK` response code and [TableRow](../resources/tablerow.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6aa3a-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6aa3a-135">Example</span></span>
<span data-ttu-id="6aa3a-136">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="6aa3a-136">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="6aa3a-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6aa3a-137">Request</span></span>
<span data-ttu-id="6aa3a-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6aa3a-138">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "tablerowcollection_itemat"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/rows/ItemAt
Content-type: application/json
Content-length: 20

{
  "index": {
  }
}
```

##### <a name="response"></a><span data-ttu-id="6aa3a-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6aa3a-139">Response</span></span>
<span data-ttu-id="6aa3a-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6aa3a-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.tableRow"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 45

{
  "index": 99,
  "values": "values-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "TableRowCollection: ItemAt",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->