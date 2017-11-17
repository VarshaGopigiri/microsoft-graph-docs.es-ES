# <a name="create-table"></a><span data-ttu-id="e53dd-101">Create Table</span><span class="sxs-lookup"><span data-stu-id="e53dd-101">Create Table</span></span>

<span data-ttu-id="e53dd-102">Use esta API para crear un objeto Table.</span><span class="sxs-lookup"><span data-stu-id="e53dd-102">Use this API to create a new Table.</span></span>
## <a name="permissions"></a><span data-ttu-id="e53dd-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="e53dd-103">Permissions</span></span>
<span data-ttu-id="e53dd-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="e53dd-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="e53dd-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e53dd-106">Permission type</span></span>      | <span data-ttu-id="e53dd-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e53dd-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e53dd-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e53dd-108">Delegated (work or school account)</span></span> | <span data-ttu-id="e53dd-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e53dd-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="e53dd-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e53dd-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e53dd-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e53dd-111">Not supported.</span></span>    |
|<span data-ttu-id="e53dd-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e53dd-112">Application</span></span> | <span data-ttu-id="e53dd-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e53dd-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="e53dd-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e53dd-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/$/add

```
## <a name="request-headers"></a><span data-ttu-id="e53dd-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e53dd-115">Request headers</span></span>
| <span data-ttu-id="e53dd-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="e53dd-116">Name</span></span>       | <span data-ttu-id="e53dd-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="e53dd-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="e53dd-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="e53dd-118">Authorization</span></span>  | <span data-ttu-id="e53dd-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e53dd-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="e53dd-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e53dd-121">Request body</span></span>
<span data-ttu-id="e53dd-122">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [Table](../resources/table.md).</span><span class="sxs-lookup"><span data-stu-id="e53dd-122">In the request body, supply a JSON representation of [Table](../resources/table.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="e53dd-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e53dd-123">Response</span></span>

<span data-ttu-id="e53dd-124">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [Table](../resources/table.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e53dd-124">If successful, this method returns `201 Created` response code and [Table](../resources/table.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e53dd-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e53dd-125">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e53dd-126">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e53dd-126">Request</span></span>
<span data-ttu-id="e53dd-127">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e53dd-127">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_table_from_workbook"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/$/add
Content-type: application/json
Content-length: 109

{
  "id": 99,
  "name": "name-value",
  "showHeaders": true,
  "showTotals": true,
  "style": "style-value"
}
```
<span data-ttu-id="e53dd-128">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [Table](../resources/table.md).</span><span class="sxs-lookup"><span data-stu-id="e53dd-128">In the request body, supply a JSON representation of [Table](../resources/table.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="e53dd-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e53dd-129">Response</span></span>
<span data-ttu-id="e53dd-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e53dd-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.table"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 109

{
  "id": "99",
  "name": "name-value",
  "showHeaders": true,
  "showTotals": true,
  "style": "style-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Table",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
