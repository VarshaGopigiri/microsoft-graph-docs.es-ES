# <a name="workbookrangeview-itemat"></a><span data-ttu-id="e1858-101">workbookRangeView: itemAt</span><span class="sxs-lookup"><span data-stu-id="e1858-101">workbookRangeView: itemAt</span></span>


## <a name="permissions"></a><span data-ttu-id="e1858-102">Permisos</span><span class="sxs-lookup"><span data-stu-id="e1858-102">Permissions</span></span>
<span data-ttu-id="e1858-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="e1858-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="e1858-105">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e1858-105">Permission type</span></span>      | <span data-ttu-id="e1858-106">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e1858-106">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e1858-107">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e1858-107">Delegated (work or school account)</span></span> | <span data-ttu-id="e1858-108">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e1858-108">Files.ReadWrite</span></span> |
|<span data-ttu-id="e1858-109">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e1858-109">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e1858-110">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e1858-110">Not supported.</span></span>    |
|<span data-ttu-id="e1858-111">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e1858-111">Application</span></span> | <span data-ttu-id="e1858-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e1858-112">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="e1858-113">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e1858-113">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET me/drive/root/workbook/worksheets/{id}/range(address={address})/visibleView/itemAt(index={n})

```
## <a name="request-headers"></a><span data-ttu-id="e1858-114">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e1858-114">Request headers</span></span>
| <span data-ttu-id="e1858-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="e1858-115">Name</span></span>       | <span data-ttu-id="e1858-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1858-116">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="e1858-117">Authorization</span><span class="sxs-lookup"><span data-stu-id="e1858-117">Authorization</span></span>  | <span data-ttu-id="e1858-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e1858-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="e1858-120">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="e1858-120">Workbook-Session-Id</span></span>  | <span data-ttu-id="e1858-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="e1858-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="function-parameters"></a><span data-ttu-id="e1858-123">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="e1858-123">Function parameters</span></span>
<span data-ttu-id="e1858-124">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="e1858-124">In the request URL, provide following query parameters with values.</span></span>

| <span data-ttu-id="e1858-125">Parámetro</span><span class="sxs-lookup"><span data-stu-id="e1858-125">Parameter</span></span>    | <span data-ttu-id="e1858-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="e1858-126">Type</span></span>   |<span data-ttu-id="e1858-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1858-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e1858-128">index</span><span class="sxs-lookup"><span data-stu-id="e1858-128">index</span></span>|<span data-ttu-id="e1858-129">Int32</span><span class="sxs-lookup"><span data-stu-id="e1858-129">Int32</span></span>|<span data-ttu-id="e1858-130">Índice del elemento que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="e1858-130">Index of the item to be returned.</span></span>|

## <a name="response"></a><span data-ttu-id="e1858-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e1858-131">Response</span></span>

<span data-ttu-id="e1858-132">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [workbookRangeView](../resources/workbookrangeview.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e1858-132">If successful, this method returns `200 OK` response code and [workbookRangeView](../resources/workbookrangeview.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e1858-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e1858-133">Example</span></span>
<span data-ttu-id="e1858-134">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="e1858-134">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="e1858-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e1858-135">Request</span></span>
<span data-ttu-id="e1858-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e1858-136">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "workbookrangeview_itemat"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/root/workbook/worksheets/{id}/range(address='A1:Z10')/visibleView/itemAt(index=0)

```

##### <a name="response"></a><span data-ttu-id="e1858-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e1858-137">Response</span></span>
<span data-ttu-id="e1858-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e1858-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
