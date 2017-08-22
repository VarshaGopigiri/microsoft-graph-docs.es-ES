# <a name="workbookrange-visibleview"></a><span data-ttu-id="0d426-101">workbookRange: visibleView</span><span class="sxs-lookup"><span data-stu-id="0d426-101">workbookRange: visibleView</span></span>


## <a name="prerequisites"></a><span data-ttu-id="0d426-102">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0d426-102">Prerequisites</span></span>
<span data-ttu-id="0d426-103">Se requieren los siguientes **ámbitos** para ejecutar esta API: _Files.Read, Files.ReadWrite_</span><span class="sxs-lookup"><span data-stu-id="0d426-103">The following **scopes** are required to execute this API: _Files.Read, Files.ReadWrite_</span></span>
## <a name="http-request"></a><span data-ttu-id="0d426-104">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0d426-104">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/drive/root/workbook/worksheets/{id}/range(address={address})/visibleView
```
## <a name="request-headers"></a><span data-ttu-id="0d426-105">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0d426-105">Request headers</span></span>
| <span data-ttu-id="0d426-106">Nombre</span><span class="sxs-lookup"><span data-stu-id="0d426-106">Name</span></span>       | <span data-ttu-id="0d426-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d426-107">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="0d426-108">Authorization</span><span class="sxs-lookup"><span data-stu-id="0d426-108">Authorization</span></span>  | <span data-ttu-id="0d426-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0d426-p101">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="0d426-111">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="0d426-111">Workbook-Session-Id</span></span>  | <span data-ttu-id="0d426-p102">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="0d426-p102">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="0d426-114">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="0d426-114">Request body</span></span>

## <a name="response"></a><span data-ttu-id="0d426-115">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0d426-115">Response</span></span>

<span data-ttu-id="0d426-116">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [workbookRangeView](../resources/workbookrangeview.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0d426-116">If successful, this method returns `200, OK` response code and [workbookRangeView](../resources/workbookrangeview.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0d426-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0d426-117">Example</span></span>
<span data-ttu-id="0d426-118">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="0d426-118">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="0d426-119">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0d426-119">Request</span></span>
<span data-ttu-id="0d426-120">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0d426-120">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "workbookrange_visibleview"
}-->
```http
GET https://graph.microsoft.com/v1.0/drive/root/workbook/worksheets/{id}/range(addres='A1:Z10')/visibleView
```

##### <a name="response"></a><span data-ttu-id="0d426-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0d426-121">Response</span></span>
<span data-ttu-id="0d426-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0d426-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookRangeView"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 194

{
  "cellAddresses": "cellAddresses-value",
  "columnCount": 99,
  "formulas": "formulas-value",
  "formulasLocal": "formulasLocal-value",
  "formulasR1C1": "formulasR1C1-value",
  "index": 99
}
```