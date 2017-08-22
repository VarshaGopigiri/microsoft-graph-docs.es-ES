# <a name="tablecolumn-headerrowrange"></a><span data-ttu-id="9fcfa-101">TableColumn: HeaderRowRange</span><span class="sxs-lookup"><span data-stu-id="9fcfa-101">TableColumn: HeaderRowRange</span></span>

<span data-ttu-id="9fcfa-102">Obtiene el objeto de rango asociado a la fila de encabezado de la columna.</span><span class="sxs-lookup"><span data-stu-id="9fcfa-102">Gets the range object associated with the header row of the column.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9fcfa-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9fcfa-103">Prerequisites</span></span>
<span data-ttu-id="9fcfa-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="9fcfa-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="9fcfa-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9fcfa-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="9fcfa-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9fcfa-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables/{id|name}/columns/{id|name}/HeaderRowRange
POST /workbook/worksheets/{id|name}/tables/{id|name}/columns/{id|name}/HeaderRowRange

```
## <a name="request-headers"></a><span data-ttu-id="9fcfa-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9fcfa-107">Request headers</span></span>
| <span data-ttu-id="9fcfa-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="9fcfa-108">Name</span></span>       | <span data-ttu-id="9fcfa-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="9fcfa-109">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="9fcfa-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="9fcfa-110">Authorization</span></span>  | <span data-ttu-id="9fcfa-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9fcfa-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="9fcfa-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9fcfa-113">Request body</span></span>

## <a name="response"></a><span data-ttu-id="9fcfa-114">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9fcfa-114">Response</span></span>

<span data-ttu-id="9fcfa-115">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9fcfa-115">If successful, this method returns `200, OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9fcfa-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9fcfa-116">Example</span></span>
<span data-ttu-id="9fcfa-117">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="9fcfa-117">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="9fcfa-118">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9fcfa-118">Request</span></span>
<span data-ttu-id="9fcfa-119">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9fcfa-119">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "tablecolumn_headerrowrange"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/columns/{id|name}/HeaderRowRange
```

##### <a name="response"></a><span data-ttu-id="9fcfa-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9fcfa-120">Response</span></span>
<span data-ttu-id="9fcfa-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9fcfa-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "TableColumn: HeaderRowRange",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->