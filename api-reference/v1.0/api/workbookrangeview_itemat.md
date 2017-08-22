# <a name="workbookrangeview-itemat"></a><span data-ttu-id="1d5a1-101">workbookRangeView: itemAt</span><span class="sxs-lookup"><span data-stu-id="1d5a1-101">workbookRangeView: itemAt</span></span>


## <a name="prerequisites"></a><span data-ttu-id="1d5a1-102">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1d5a1-102">Prerequisites</span></span>
<span data-ttu-id="1d5a1-103">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="1d5a1-103">The following **scopes** are required to execute this API:</span></span>
## <a name="http-request"></a><span data-ttu-id="1d5a1-104">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1d5a1-104">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET me/drive/root/workbook/worksheets/{id}/range(addres={address})/visibleView/itemAt(index={n})

```
## <a name="request-headers"></a><span data-ttu-id="1d5a1-105">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1d5a1-105">Request headers</span></span>
| <span data-ttu-id="1d5a1-106">Nombre</span><span class="sxs-lookup"><span data-stu-id="1d5a1-106">Name</span></span>       | <span data-ttu-id="1d5a1-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d5a1-107">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="1d5a1-108">Authorization</span><span class="sxs-lookup"><span data-stu-id="1d5a1-108">Authorization</span></span>  | <span data-ttu-id="1d5a1-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1d5a1-p101">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="1d5a1-111">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="1d5a1-111">Workbook-Session-Id</span></span>  | <span data-ttu-id="1d5a1-p102">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="1d5a1-p102">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="1d5a1-114">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="1d5a1-114">Request body</span></span>
<span data-ttu-id="1d5a1-115">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="1d5a1-115">In the request URL, provide following query parameters with values.</span></span>

| <span data-ttu-id="1d5a1-116">Parámetro</span><span class="sxs-lookup"><span data-stu-id="1d5a1-116">Parameter</span></span>    | <span data-ttu-id="1d5a1-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="1d5a1-117">Type</span></span>   |<span data-ttu-id="1d5a1-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="1d5a1-118">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1d5a1-119">index</span><span class="sxs-lookup"><span data-stu-id="1d5a1-119">index</span></span>|<span data-ttu-id="1d5a1-120">Int32</span><span class="sxs-lookup"><span data-stu-id="1d5a1-120">Int32</span></span>|<span data-ttu-id="1d5a1-121">Índice del elemento que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="1d5a1-121">Index of the item to be returned.</span></span>|

## <a name="response"></a><span data-ttu-id="1d5a1-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1d5a1-122">Response</span></span>

<span data-ttu-id="1d5a1-123">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [workbookRangeView](../resources/workbookrangeview.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1d5a1-123">If successful, this method returns `200, OK` response code and [workbookRangeView](../resources/workbookrangeview.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1d5a1-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1d5a1-124">Example</span></span>
<span data-ttu-id="1d5a1-125">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="1d5a1-125">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="1d5a1-126">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1d5a1-126">Request</span></span>
<span data-ttu-id="1d5a1-127">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1d5a1-127">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "workbookrangeview_itemat"
}-->
```http
GET https://graph.microsoft.com/v1.0/drive/root/workbook/worksheets/{id}/range(addres='A1:Z10')/visibleView/itemAt(index=0)

```

##### <a name="response"></a><span data-ttu-id="1d5a1-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1d5a1-128">Response</span></span>
<span data-ttu-id="1d5a1-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1d5a1-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
