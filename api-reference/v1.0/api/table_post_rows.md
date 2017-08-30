# <a name="create-tablerow"></a><span data-ttu-id="cf075-101">Create TableRow</span><span class="sxs-lookup"><span data-stu-id="cf075-101">Create TableRow</span></span>

<span data-ttu-id="cf075-102">Use esta API para crear un objeto TableRow.</span><span class="sxs-lookup"><span data-stu-id="cf075-102">Use this API to create a new TableRow.</span></span>
## <a name="permissions"></a><span data-ttu-id="cf075-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="cf075-103">Permissions</span></span>
<span data-ttu-id="cf075-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="cf075-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="cf075-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cf075-106">Permission type</span></span>      | <span data-ttu-id="cf075-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cf075-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="cf075-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cf075-108">Delegated (work or school account)</span></span> | <span data-ttu-id="cf075-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="cf075-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="cf075-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cf075-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="cf075-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cf075-111">Not supported.</span></span>    |
|<span data-ttu-id="cf075-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cf075-112">Application</span></span> | <span data-ttu-id="cf075-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cf075-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="cf075-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cf075-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/rows
POST /workbook/worksheets/{id|name}/tables/{id|name}/rows

```
## <a name="request-headers"></a><span data-ttu-id="cf075-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cf075-115">Request headers</span></span>
| <span data-ttu-id="cf075-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="cf075-116">Name</span></span>       | <span data-ttu-id="cf075-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf075-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="cf075-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="cf075-118">Authorization</span></span>  | <span data-ttu-id="cf075-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cf075-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="cf075-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cf075-121">Request body</span></span>
<span data-ttu-id="cf075-122">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [TableRow](../resources/tablerow.md).</span><span class="sxs-lookup"><span data-stu-id="cf075-122">In the request body, supply a JSON representation of [TableRow](../resources/tablerow.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="cf075-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cf075-123">Response</span></span>

<span data-ttu-id="cf075-124">Si se ejecuta correctamente, este método devuelve un código de respuesta `201, Created` y el objeto [TableRow](../resources/tablerow.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cf075-124">If successful, this method returns `201, Created` response code and [TableRow](../resources/tablerow.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cf075-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cf075-125">Example</span></span>
##### <a name="request"></a><span data-ttu-id="cf075-126">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cf075-126">Request</span></span>
<span data-ttu-id="cf075-127">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cf075-127">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_tablerow_from_table"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/rows
Content-type: application/json
Content-length: 45

{
  "index": 99,
  "values": "values-value"
}
```
<span data-ttu-id="cf075-128">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [TableRow](../resources/tablerow.md).</span><span class="sxs-lookup"><span data-stu-id="cf075-128">In the request body, supply a JSON representation of [TableRow](../resources/tablerow.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="cf075-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cf075-129">Response</span></span>
<span data-ttu-id="cf075-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cf075-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.tableRow"
} -->
```http
HTTP/1.1 201 Created
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
  "description": "Create TableRow",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->