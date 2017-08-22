# <a name="workbookrangeview-range"></a><span data-ttu-id="2c2c9-101">workbookRangeView: range</span><span class="sxs-lookup"><span data-stu-id="2c2c9-101">workbookRangeView: range</span></span>
<span data-ttu-id="2c2c9-102">Devuelve un rango asociado al recurso rangeView.</span><span class="sxs-lookup"><span data-stu-id="2c2c9-102">Return the range associated with the rangeView resource.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2c2c9-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2c2c9-103">Prerequisites</span></span>
<span data-ttu-id="2c2c9-104">Se requieren los siguientes **ámbitos** para ejecutar esta API: _Files.Read, Files.ReadWrite_</span><span class="sxs-lookup"><span data-stu-id="2c2c9-104">The following **scopes** are required to execute this API: _Files.Read, Files.ReadWrite_</span></span>

## <a name="http-request"></a><span data-ttu-id="2c2c9-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2c2c9-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET me/drive/root/workbook/worksheets/{id}/range(addres={address})/visibleView/range

```
## <a name="request-headers"></a><span data-ttu-id="2c2c9-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2c2c9-106">Request headers</span></span>
| <span data-ttu-id="2c2c9-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="2c2c9-107">Name</span></span>       | <span data-ttu-id="2c2c9-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c2c9-108">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="2c2c9-109">Authorization</span><span class="sxs-lookup"><span data-stu-id="2c2c9-109">Authorization</span></span>  | <span data-ttu-id="2c2c9-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2c2c9-p101">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="2c2c9-112">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="2c2c9-112">Workbook-Session-Id</span></span>  | <span data-ttu-id="2c2c9-p102">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="2c2c9-p102">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="2c2c9-115">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="2c2c9-115">Request body</span></span>

## <a name="response"></a><span data-ttu-id="2c2c9-116">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2c2c9-116">Response</span></span>

<span data-ttu-id="2c2c9-117">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [workbookRange](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2c2c9-117">If successful, this method returns `200, OK` response code and [workbookRange](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2c2c9-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2c2c9-118">Example</span></span>
<span data-ttu-id="2c2c9-119">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="2c2c9-119">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="2c2c9-120">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2c2c9-120">Request</span></span>
<span data-ttu-id="2c2c9-121">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2c2c9-121">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "workbookrangeview_range"
}-->
```http
GET https://graph.microsoft.com/v1.0/drive/root/workbook/worksheets/{id}/range(addres='A1:Z10')/visibleView/range
```

##### <a name="response"></a><span data-ttu-id="2c2c9-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2c2c9-122">Response</span></span>
<span data-ttu-id="2c2c9-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2c2c9-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.range"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 157

{
  "address": "address-value",
  "addressLocal": "addressLocal-value",
  "cellCount": 99,
  "columnCount": 99,
  "columnHidden": true,
  "columnIndex": 99
}
```
