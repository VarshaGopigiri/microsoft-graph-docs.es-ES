# <a name="table-converttorange"></a><span data-ttu-id="60dc0-101">Table: convertToRange</span><span class="sxs-lookup"><span data-stu-id="60dc0-101">Table: convertToRange</span></span>

<span data-ttu-id="60dc0-p101">Convierte la tabla en un rango de celdas normal. Se conservan todos los datos.</span><span class="sxs-lookup"><span data-stu-id="60dc0-p101">Converts the table into a normal range of cells. All data is preserved.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="60dc0-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="60dc0-104">Prerequisites</span></span>
<span data-ttu-id="60dc0-105">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="60dc0-105">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="60dc0-106">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="60dc0-106">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="60dc0-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="60dc0-107">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/convertToRange
POST /workbook/worksheets/{id|name}/tables/{id|name}/convertToRange

```
## <a name="request-headers"></a><span data-ttu-id="60dc0-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="60dc0-108">Request headers</span></span>
| <span data-ttu-id="60dc0-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="60dc0-109">Name</span></span>       | <span data-ttu-id="60dc0-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="60dc0-110">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="60dc0-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="60dc0-111">Authorization</span></span>  | <span data-ttu-id="60dc0-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="60dc0-p102">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="60dc0-114">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="60dc0-114">Request body</span></span>

## <a name="response"></a><span data-ttu-id="60dc0-115">Respuesta</span><span class="sxs-lookup"><span data-stu-id="60dc0-115">Response</span></span>

<span data-ttu-id="60dc0-116">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="60dc0-116">If successful, this method returns `200, OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="60dc0-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="60dc0-117">Example</span></span>
<span data-ttu-id="60dc0-118">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="60dc0-118">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="60dc0-119">Solicitud</span><span class="sxs-lookup"><span data-stu-id="60dc0-119">Request</span></span>
<span data-ttu-id="60dc0-120">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="60dc0-120">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "table_converttorange"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/convertToRange
```

##### <a name="response"></a><span data-ttu-id="60dc0-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="60dc0-121">Response</span></span>
<span data-ttu-id="60dc0-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="60dc0-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Table: convertToRange",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->