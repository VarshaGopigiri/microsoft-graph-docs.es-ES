# <a name="range-entirerow"></a><span data-ttu-id="b4c41-101">Range: EntireRow</span><span class="sxs-lookup"><span data-stu-id="b4c41-101">Range: EntireRow</span></span>

<span data-ttu-id="b4c41-102">Obtiene un objeto que representa toda la fila del intervalo.</span><span class="sxs-lookup"><span data-stu-id="b4c41-102">Gets an object that represents the entire row of the range.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b4c41-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b4c41-103">Prerequisites</span></span>
<span data-ttu-id="b4c41-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="b4c41-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="b4c41-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b4c41-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="b4c41-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b4c41-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names(<name>)/range/EntireRow
GET /workbook/worksheets/{id|name}/range(<address>)/EntireRow
GET /workbook/tables/{id|name}/columns/{id|name}/range/EntireRow

```
## <a name="request-headers"></a><span data-ttu-id="b4c41-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b4c41-107">Request headers</span></span>
| <span data-ttu-id="b4c41-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="b4c41-108">Name</span></span>       | <span data-ttu-id="b4c41-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4c41-109">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="b4c41-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="b4c41-110">Authorization</span></span>  | <span data-ttu-id="b4c41-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b4c41-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="b4c41-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b4c41-113">Request body</span></span>

## <a name="response"></a><span data-ttu-id="b4c41-114">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b4c41-114">Response</span></span>

<span data-ttu-id="b4c41-115">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b4c41-115">If successful, this method returns `200, OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b4c41-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b4c41-116">Example</span></span>
<span data-ttu-id="b4c41-117">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="b4c41-117">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="b4c41-118">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b4c41-118">Request</span></span>
<span data-ttu-id="b4c41-119">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b4c41-119">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_entirerow"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/range/EntireRow
```

##### <a name="response"></a><span data-ttu-id="b4c41-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b4c41-120">Response</span></span>
<span data-ttu-id="b4c41-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b4c41-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.range"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 169

{
  "address": "address-value",
  "addressLocal": "addressLocal-value",
  "cellCount": 99,
  "columnCount": 99,
  "columnIndex": 99,
  "valueTypes": "valueTypes-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Range: EntireRow",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->