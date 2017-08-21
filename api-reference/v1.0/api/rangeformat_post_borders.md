# <a name="create-rangeborder"></a><span data-ttu-id="49177-101">Create RangeBorder</span><span class="sxs-lookup"><span data-stu-id="49177-101">Create RangeBorder</span></span>

<span data-ttu-id="49177-102">Use esta API para crear un objeto RangeBorder.</span><span class="sxs-lookup"><span data-stu-id="49177-102">Use this API to create a new RangeBorder.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="49177-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="49177-103">Prerequisites</span></span>
<span data-ttu-id="49177-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="49177-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="49177-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="49177-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="49177-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="49177-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names(<name>)/range/format/borders
POST /workbook/worksheets/{id|name}/range(<address>)/format/borders
POST /workbook/tables/{id|name}/columns/{id|name}/range/format/borders

```
## <a name="request-headers"></a><span data-ttu-id="49177-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="49177-107">Request headers</span></span>
| <span data-ttu-id="49177-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="49177-108">Name</span></span>       | <span data-ttu-id="49177-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="49177-109">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="49177-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="49177-110">Authorization</span></span>  | <span data-ttu-id="49177-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="49177-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="49177-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="49177-113">Request body</span></span>
<span data-ttu-id="49177-114">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [RangeBorder](../resources/rangeborder.md).</span><span class="sxs-lookup"><span data-stu-id="49177-114">In the request body, supply a JSON representation of [RangeBorder](../resources/rangeborder.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="49177-115">Respuesta</span><span class="sxs-lookup"><span data-stu-id="49177-115">Response</span></span>

<span data-ttu-id="49177-116">Si se ejecuta correctamente, este método devuelve un código de respuesta `201, Created` y el objeto [RangeBorder](../resources/rangeborder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="49177-116">If successful, this method returns `201, Created` response code and [RangeBorder](../resources/rangeborder.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="49177-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="49177-117">Example</span></span>
##### <a name="request"></a><span data-ttu-id="49177-118">Solicitud</span><span class="sxs-lookup"><span data-stu-id="49177-118">Request</span></span>
<span data-ttu-id="49177-119">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="49177-119">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_rangeborder_from_rangeformat"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/range/format/borders
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
<span data-ttu-id="49177-120">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [RangeBorder](../resources/rangeborder.md).</span><span class="sxs-lookup"><span data-stu-id="49177-120">In the request body, supply a JSON representation of [RangeBorder](../resources/rangeborder.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="49177-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="49177-121">Response</span></span>
<span data-ttu-id="49177-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="49177-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.rangeBorder"
} -->
```http
HTTP/1.1 201 Created
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
  "description": "Create RangeBorder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->