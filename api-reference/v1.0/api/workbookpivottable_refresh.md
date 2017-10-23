# <a name="workbookpivottable-refresh"></a><span data-ttu-id="0543c-101">workbookPivotTable: refresh</span><span class="sxs-lookup"><span data-stu-id="0543c-101">workbookPivotTable: refresh</span></span>

<span data-ttu-id="0543c-102">Actualiza la tabla dinámica.</span><span class="sxs-lookup"><span data-stu-id="0543c-102">Refreshes the PivotTable.</span></span>


## <a name="permissions"></a><span data-ttu-id="0543c-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="0543c-103">Permissions</span></span>
<span data-ttu-id="0543c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="0543c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="0543c-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0543c-106">Permission type</span></span>      | <span data-ttu-id="0543c-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0543c-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0543c-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0543c-108">Delegated (work or school account)</span></span> | <span data-ttu-id="0543c-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0543c-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="0543c-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0543c-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0543c-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0543c-111">Not supported.</span></span>    |
|<span data-ttu-id="0543c-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0543c-112">Application</span></span> | <span data-ttu-id="0543c-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0543c-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="0543c-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0543c-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/drive/root/workbook/worksheets/{id}/pivotTables/{id}/refresh
```
## <a name="request-headers"></a><span data-ttu-id="0543c-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0543c-115">Request headers</span></span>
| <span data-ttu-id="0543c-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="0543c-116">Name</span></span>       | <span data-ttu-id="0543c-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="0543c-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="0543c-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="0543c-118">Authorization</span></span>  | <span data-ttu-id="0543c-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0543c-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="0543c-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="0543c-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="0543c-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="0543c-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="0543c-124">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="0543c-124">Request body</span></span>

### <a name="response"></a><span data-ttu-id="0543c-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0543c-125">Response</span></span>
<span data-ttu-id="0543c-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0543c-p104">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0543c-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0543c-128">Example</span></span>
<span data-ttu-id="0543c-129">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="0543c-129">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="0543c-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0543c-130">Request</span></span>
<span data-ttu-id="0543c-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0543c-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "workbookpivottable_refresh"
}-->
```http
POST https://graph.microsoft.com/v1.0/drive/root/workbook/worksheets/{id}/pivotTables/{id}/refresh
```

##### <a name="response"></a><span data-ttu-id="0543c-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0543c-132">Response</span></span>
<span data-ttu-id="0543c-133">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0543c-133">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.none"
} -->
```http
HTTP/1.1 200 OK
```
