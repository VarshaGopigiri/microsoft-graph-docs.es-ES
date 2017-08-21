# <a name="worksheet-cell"></a><span data-ttu-id="10844-101">Worksheet: Cell</span><span class="sxs-lookup"><span data-stu-id="10844-101">Worksheet: Cell</span></span>

<span data-ttu-id="10844-p101">Obtiene el objeto de rango que contiene la celda en función de los números de fila y columna. La celda puede estar fuera de los límites del rango principal, siempre y cuando permanezca dentro de la cuadrícula de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="10844-p101">Gets the range object containing the single cell based on row and column numbers. The cell can be outside the bounds of its parent range, so long as it's stays within the worksheet grid.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="10844-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="10844-104">Prerequisites</span></span>
<span data-ttu-id="10844-105">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="10844-105">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="10844-106">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="10844-106">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="10844-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="10844-107">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/worksheets/{id|name}/Cell(row=<row>,column=<column>)

```
## <a name="request-headers"></a><span data-ttu-id="10844-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="10844-108">Request headers</span></span>
| <span data-ttu-id="10844-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="10844-109">Name</span></span>       | <span data-ttu-id="10844-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="10844-110">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="10844-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="10844-111">Authorization</span></span>  | <span data-ttu-id="10844-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="10844-p102">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="10844-114">Respuesta</span><span class="sxs-lookup"><span data-stu-id="10844-114">Response</span></span>

<span data-ttu-id="10844-115">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="10844-115">If successful, this method returns `200, OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="10844-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="10844-116">Example</span></span>
<span data-ttu-id="10844-117">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="10844-117">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="10844-118">Solicitud</span><span class="sxs-lookup"><span data-stu-id="10844-118">Request</span></span>
<span data-ttu-id="10844-119">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="10844-119">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "worksheet_cell"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/Cell(row=<row>,column=<column>)
```

##### <a name="response"></a><span data-ttu-id="10844-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="10844-120">Response</span></span>
<span data-ttu-id="10844-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="10844-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "cellCount": 1,
  "columnCount": 1,
  "columnIndex": 3,
  "valueTypes": "valueTypes-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Worksheet: Cell",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
