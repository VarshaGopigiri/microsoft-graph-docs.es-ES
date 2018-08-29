# <a name="workbookrangeview-range"></a><span data-ttu-id="70617-101">workbookRangeView: range</span><span class="sxs-lookup"><span data-stu-id="70617-101">workbookRangeView: range</span></span>
<span data-ttu-id="70617-102">Devolver el rango asociado al recurso rangeView.</span><span class="sxs-lookup"><span data-stu-id="70617-102">Return the range associated with the rangeView resource.</span></span>

## <a name="permissions"></a><span data-ttu-id="70617-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="70617-103">Permissions</span></span>
<span data-ttu-id="70617-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="70617-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="70617-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="70617-106">Permission type</span></span>      | <span data-ttu-id="70617-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="70617-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="70617-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="70617-108">Delegated (work or school account)</span></span> | <span data-ttu-id="70617-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="70617-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="70617-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="70617-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="70617-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="70617-111">Not supported.</span></span>    |
|<span data-ttu-id="70617-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="70617-112">Application</span></span> | <span data-ttu-id="70617-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="70617-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="70617-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="70617-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET me/drive/root/workbook/worksheets/{id}/range(address={address})/visibleView/range

```
## <a name="request-headers"></a><span data-ttu-id="70617-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="70617-115">Request headers</span></span>
| <span data-ttu-id="70617-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="70617-116">Name</span></span>       | <span data-ttu-id="70617-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="70617-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="70617-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="70617-118">Authorization</span></span>  | <span data-ttu-id="70617-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="70617-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="70617-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="70617-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="70617-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="70617-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="70617-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="70617-124">Request body</span></span>

### <a name="response"></a><span data-ttu-id="70617-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="70617-125">Response</span></span>
<span data-ttu-id="70617-126">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [workbookRange](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="70617-126">If successful, this method returns `200 OK` response code and [workbookRange](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="70617-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="70617-127">Example</span></span>
<span data-ttu-id="70617-128">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="70617-128">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="70617-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="70617-129">Request</span></span>
<span data-ttu-id="70617-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="70617-130">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "workbookrangeview_range"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/root/workbook/worksheets/{id}/range(address='A1:Z10')/visibleView/range
```

##### <a name="response"></a><span data-ttu-id="70617-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="70617-131">Response</span></span>
<span data-ttu-id="70617-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="70617-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookRange"
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
