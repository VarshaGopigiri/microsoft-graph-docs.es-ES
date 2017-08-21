# <a name="create-tablerow"></a><span data-ttu-id="3bb7d-101">Create TableRow</span><span class="sxs-lookup"><span data-stu-id="3bb7d-101">Create TableRow</span></span>

<span data-ttu-id="3bb7d-102">Use esta API para crear un objeto TableRow.</span><span class="sxs-lookup"><span data-stu-id="3bb7d-102">Use this API to create a new TableRow.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3bb7d-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3bb7d-103">Prerequisites</span></span>
<span data-ttu-id="3bb7d-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="3bb7d-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="3bb7d-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3bb7d-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="3bb7d-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3bb7d-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/rows
POST /workbook/worksheets/{id|name}/tables/{id|name}/rows

```
## <a name="request-headers"></a><span data-ttu-id="3bb7d-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3bb7d-107">Request headers</span></span>
| <span data-ttu-id="3bb7d-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="3bb7d-108">Name</span></span>       | <span data-ttu-id="3bb7d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="3bb7d-109">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="3bb7d-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="3bb7d-110">Authorization</span></span>  | <span data-ttu-id="3bb7d-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3bb7d-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="3bb7d-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3bb7d-113">Request body</span></span>
<span data-ttu-id="3bb7d-114">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [TableRow](../resources/tablerow.md).</span><span class="sxs-lookup"><span data-stu-id="3bb7d-114">In the request body, supply a JSON representation of [TableRow](../resources/tablerow.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="3bb7d-115">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3bb7d-115">Response</span></span>

<span data-ttu-id="3bb7d-116">Si se ejecuta correctamente, este método devuelve un código de respuesta `201, Created` y el objeto [TableRow](../resources/tablerow.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3bb7d-116">If successful, this method returns `201, Created` response code and [TableRow](../resources/tablerow.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3bb7d-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3bb7d-117">Example</span></span>
##### <a name="request"></a><span data-ttu-id="3bb7d-118">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3bb7d-118">Request</span></span>
<span data-ttu-id="3bb7d-119">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3bb7d-119">Here is an example of the request.</span></span>
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
<span data-ttu-id="3bb7d-120">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [TableRow](../resources/tablerow.md).</span><span class="sxs-lookup"><span data-stu-id="3bb7d-120">In the request body, supply a JSON representation of [TableRow](../resources/tablerow.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="3bb7d-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3bb7d-121">Response</span></span>
<span data-ttu-id="3bb7d-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3bb7d-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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