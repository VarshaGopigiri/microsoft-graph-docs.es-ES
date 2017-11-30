# <a name="close-session"></a><span data-ttu-id="b2d9f-101">Cerrar sesión</span><span class="sxs-lookup"><span data-stu-id="b2d9f-101">Close Session</span></span>

<span data-ttu-id="b2d9f-102">Use esta API para cerrar una sesión existente del libro.</span><span class="sxs-lookup"><span data-stu-id="b2d9f-102">Use this API to close an existing workbook session.</span></span> 

## <a name="permissions"></a><span data-ttu-id="b2d9f-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="b2d9f-103">Permissions</span></span>
<span data-ttu-id="b2d9f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="b2d9f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="b2d9f-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b2d9f-106">Permission type</span></span>      | <span data-ttu-id="b2d9f-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b2d9f-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b2d9f-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b2d9f-108">Delegated (work or school account)</span></span> | <span data-ttu-id="b2d9f-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b2d9f-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="b2d9f-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b2d9f-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b2d9f-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b2d9f-111">Not supported.</span></span>    |
|<span data-ttu-id="b2d9f-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b2d9f-112">Application</span></span> | <span data-ttu-id="b2d9f-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b2d9f-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="b2d9f-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b2d9f-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/closeSession
workbook-session-id: {session-id}
```
## <a name="request-headers"></a><span data-ttu-id="b2d9f-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b2d9f-115">Request headers</span></span>
| <span data-ttu-id="b2d9f-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="b2d9f-116">Name</span></span>       | <span data-ttu-id="b2d9f-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2d9f-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="b2d9f-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="b2d9f-118">Authorization</span></span>  | <span data-ttu-id="b2d9f-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b2d9f-p102">Bearer {token}. Required.</span></span> | | <span data-ttu-id="b2d9f-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="b2d9f-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="b2d9f-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="b2d9f-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|
| <span data-ttu-id="b2d9f-124">workbook-session-id</span><span class="sxs-lookup"><span data-stu-id="b2d9f-124">workbook-session-id</span></span> | <span data-ttu-id="b2d9f-125">Workbook session Id que se va a cerrar</span><span class="sxs-lookup"><span data-stu-id="b2d9f-125">Workbook session Id to be closed</span></span> |

## <a name="request-body"></a><span data-ttu-id="b2d9f-126">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="b2d9f-126">Request body</span></span>
<span data-ttu-id="b2d9f-127">Esta API no requiere ningún cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b2d9f-127">This API does not require any request body.</span></span>

## <a name="response"></a><span data-ttu-id="b2d9f-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b2d9f-128">Response</span></span>

<span data-ttu-id="b2d9f-129">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="b2d9f-129">If successful, this method returns `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="b2d9f-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b2d9f-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b2d9f-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b2d9f-131">Request</span></span>
<span data-ttu-id="b2d9f-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b2d9f-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "close_excel_session"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/closeSession
Content-type: application/json
workbook-session-id: {session-id}
Content-length: 0

{

}
```

<span data-ttu-id="b2d9f-133">Tenga en cuenta que se necesita dicho encabezado workbook-session-id.</span><span class="sxs-lookup"><span data-stu-id="b2d9f-133">Note that workbook-session-id header is required.</span></span> 


##### <a name="response"></a><span data-ttu-id="b2d9f-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b2d9f-134">Response</span></span>
<span data-ttu-id="b2d9f-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b2d9f-135">Here is an example of the response.</span></span> 

<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```