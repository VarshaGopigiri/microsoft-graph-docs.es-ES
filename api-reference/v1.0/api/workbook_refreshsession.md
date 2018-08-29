# <a name="refresh-session"></a><span data-ttu-id="63603-101">Actualizar sesión</span><span class="sxs-lookup"><span data-stu-id="63603-101">Refresh Session</span></span>

<span data-ttu-id="63603-102">Use esta API para actualizar una sesión existente del libro.</span><span class="sxs-lookup"><span data-stu-id="63603-102">Use this API to refresh an existing workbook session.</span></span> 

## <a name="permissions"></a><span data-ttu-id="63603-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="63603-103">Permissions</span></span>
<span data-ttu-id="63603-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="63603-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="63603-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="63603-106">Permission type</span></span>      | <span data-ttu-id="63603-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="63603-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="63603-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="63603-108">Delegated (work or school account)</span></span> | <span data-ttu-id="63603-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="63603-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="63603-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="63603-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="63603-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="63603-111">Not supported.</span></span>    |
|<span data-ttu-id="63603-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="63603-112">Application</span></span> | <span data-ttu-id="63603-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="63603-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="63603-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="63603-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/refreshSession
workbook-session-id: {session-id}
```
## <a name="request-headers"></a><span data-ttu-id="63603-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="63603-115">Request headers</span></span>
| <span data-ttu-id="63603-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="63603-116">Name</span></span>       | <span data-ttu-id="63603-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="63603-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="63603-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="63603-118">Authorization</span></span>  | <span data-ttu-id="63603-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="63603-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="63603-121">workbook-session-id</span><span class="sxs-lookup"><span data-stu-id="63603-121">workbook-session-id</span></span> | <span data-ttu-id="63603-122">Id. de sesión del libro que se va a actualizar</span><span class="sxs-lookup"><span data-stu-id="63603-122">Workbook session Id to be refreshed</span></span> |

## <a name="request-body"></a><span data-ttu-id="63603-123">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="63603-123">Request body</span></span>
<span data-ttu-id="63603-124">Esta API no requiere ningún cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="63603-124">This API does not require any request body.</span></span>

## <a name="response"></a><span data-ttu-id="63603-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="63603-125">Response</span></span>

<span data-ttu-id="63603-126">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="63603-126">If successful, this method returns `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="63603-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="63603-127">Example</span></span>
##### <a name="request"></a><span data-ttu-id="63603-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="63603-128">Request</span></span>
<span data-ttu-id="63603-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="63603-129">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "refresh_excel_session"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/refreshSession
Content-type: application/json
workbook-session-id: {session-id}
Content-length: 0

{

}
```

<span data-ttu-id="63603-130">Tenga en cuenta que se necesita dicho encabezado workbook-session-id.</span><span class="sxs-lookup"><span data-stu-id="63603-130">Note that workbook-session-id header is required.</span></span> 


##### <a name="response"></a><span data-ttu-id="63603-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="63603-131">Response</span></span>
<span data-ttu-id="63603-132">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="63603-132">Here is an example of the response.</span></span> 

<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- {
  "type": "#page.annotation",
  "suppressions": [
    "Warning: refresh_excel_session//api-reference/v1.0/api/workbook_refreshsession.md:
      Request includes a non-standard header: workbook-session-id"
  ]
}-->
