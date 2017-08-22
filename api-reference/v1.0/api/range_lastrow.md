# <a name="range-lastrow"></a><span data-ttu-id="8a9b9-101">Range: LastRow</span><span class="sxs-lookup"><span data-stu-id="8a9b9-101">Range: LastRow</span></span>

<span data-ttu-id="8a9b9-p101">Obtiene la última fila del intervalo. Por ejemplo, la última fila de "B2:D5" es "B5:D5".</span><span class="sxs-lookup"><span data-stu-id="8a9b9-p101">Gets the last row within the range. For example, the last row of "B2:D5" is "B5:D5".</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8a9b9-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8a9b9-104">Prerequisites</span></span>
<span data-ttu-id="8a9b9-105">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="8a9b9-105">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="8a9b9-106">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8a9b9-106">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="8a9b9-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8a9b9-107">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names(<name>)/range/LastRow
GET /workbook/worksheets/{id|name}/range(<address>)/LastRow
GET /workbook/tables/{id|name}/columns/{id|name}/range/LastRow

```
## <a name="request-headers"></a><span data-ttu-id="8a9b9-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8a9b9-108">Request headers</span></span>
| <span data-ttu-id="8a9b9-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="8a9b9-109">Name</span></span>       | <span data-ttu-id="8a9b9-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="8a9b9-110">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="8a9b9-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="8a9b9-111">Authorization</span></span>  | <span data-ttu-id="8a9b9-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8a9b9-p102">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="8a9b9-114">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8a9b9-114">Request body</span></span>

## <a name="response"></a><span data-ttu-id="8a9b9-115">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8a9b9-115">Response</span></span>

<span data-ttu-id="8a9b9-116">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8a9b9-116">If successful, this method returns `200, OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8a9b9-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8a9b9-117">Example</span></span>
<span data-ttu-id="8a9b9-118">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="8a9b9-118">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="8a9b9-119">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8a9b9-119">Request</span></span>
<span data-ttu-id="8a9b9-120">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8a9b9-120">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_lastrow"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/range/LastRow
```

##### <a name="response"></a><span data-ttu-id="8a9b9-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8a9b9-121">Response</span></span>
<span data-ttu-id="8a9b9-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8a9b9-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Range: LastRow",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->