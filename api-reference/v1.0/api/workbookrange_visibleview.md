# <a name="workbookrange-visibleview"></a><span data-ttu-id="983ab-101">workbookRange: visibleView</span><span class="sxs-lookup"><span data-stu-id="983ab-101">workbookRange: visibleView</span></span>


## <a name="permissions"></a><span data-ttu-id="983ab-102">Permisos</span><span class="sxs-lookup"><span data-stu-id="983ab-102">Permissions</span></span>
<span data-ttu-id="983ab-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="983ab-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="983ab-105">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="983ab-105">Permission type</span></span>      | <span data-ttu-id="983ab-106">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="983ab-106">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="983ab-107">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="983ab-107">Delegated (work or school account)</span></span> | <span data-ttu-id="983ab-108">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="983ab-108">Files.ReadWrite</span></span>    |
|<span data-ttu-id="983ab-109">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="983ab-109">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="983ab-110">No admitida.</span><span class="sxs-lookup"><span data-stu-id="983ab-110">Not supported.</span></span>    |
|<span data-ttu-id="983ab-111">Aplicación</span><span class="sxs-lookup"><span data-stu-id="983ab-111">Application</span></span> | <span data-ttu-id="983ab-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="983ab-112">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="983ab-113">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="983ab-113">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/drive/root/workbook/worksheets/{id}/range(address={address})/visibleView
```
## <a name="request-headers"></a><span data-ttu-id="983ab-114">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="983ab-114">Request headers</span></span>
| <span data-ttu-id="983ab-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="983ab-115">Name</span></span>       | <span data-ttu-id="983ab-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="983ab-116">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="983ab-117">Authorization</span><span class="sxs-lookup"><span data-stu-id="983ab-117">Authorization</span></span>  | <span data-ttu-id="983ab-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="983ab-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="983ab-120">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="983ab-120">Workbook-Session-Id</span></span>  | <span data-ttu-id="983ab-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="983ab-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="983ab-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="983ab-123">Request body</span></span>

### <a name="response"></a><span data-ttu-id="983ab-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="983ab-124">Response</span></span>
<span data-ttu-id="983ab-125">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [workbookRangeView](../resources/workbookrangeview.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="983ab-125">If successful, this method returns `200 OK` response code and [workbookRangeView](../resources/workbookrangeview.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="983ab-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="983ab-126">Example</span></span>
<span data-ttu-id="983ab-127">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="983ab-127">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="983ab-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="983ab-128">Request</span></span>
<span data-ttu-id="983ab-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="983ab-129">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "workbookrange_visibleview"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/root/workbook/worksheets/{id}/range(address='A1:Z10')/visibleView
```

##### <a name="response"></a><span data-ttu-id="983ab-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="983ab-130">Response</span></span>
<span data-ttu-id="983ab-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="983ab-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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