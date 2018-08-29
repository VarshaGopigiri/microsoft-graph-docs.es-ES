# <a name="close-session"></a><span data-ttu-id="9b371-101">Cerrar sesión</span><span class="sxs-lookup"><span data-stu-id="9b371-101">Close Session</span></span>

<span data-ttu-id="9b371-102">Use esta API para cerrar una sesión existente del libro.</span><span class="sxs-lookup"><span data-stu-id="9b371-102">Use this API to close an existing workbook session.</span></span> 

## <a name="permissions"></a><span data-ttu-id="9b371-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="9b371-103">Permissions</span></span>
<span data-ttu-id="9b371-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="9b371-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="9b371-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9b371-106">Permission type</span></span>      | <span data-ttu-id="9b371-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9b371-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9b371-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9b371-108">Delegated (work or school account)</span></span> | <span data-ttu-id="9b371-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9b371-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="9b371-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9b371-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9b371-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9b371-111">Not supported.</span></span>    |
|<span data-ttu-id="9b371-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9b371-112">Application</span></span> | <span data-ttu-id="9b371-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9b371-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="9b371-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9b371-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/closeSession
workbook-session-id: {session-id}
```
## <a name="request-headers"></a><span data-ttu-id="9b371-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9b371-115">Request headers</span></span>
| <span data-ttu-id="9b371-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="9b371-116">Name</span></span>       | <span data-ttu-id="9b371-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b371-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="9b371-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="9b371-118">Authorization</span></span>  | <span data-ttu-id="9b371-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9b371-p102">Bearer {token}. Required.</span></span> | | <span data-ttu-id="9b371-121">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="9b371-121">Workbook-Session-Id</span></span>  | <span data-ttu-id="9b371-p103">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="9b371-p103">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|
| <span data-ttu-id="9b371-124">workbook-session-id</span><span class="sxs-lookup"><span data-stu-id="9b371-124">workbook-session-id</span></span> | <span data-ttu-id="9b371-125">Workbook session Id que se va a cerrar</span><span class="sxs-lookup"><span data-stu-id="9b371-125">Workbook session Id to be closed</span></span> |

## <a name="request-body"></a><span data-ttu-id="9b371-126">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="9b371-126">Request body</span></span>
<span data-ttu-id="9b371-127">Esta API no requiere ningún cuerpo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9b371-127">This API does not require any request body.</span></span>

## <a name="response"></a><span data-ttu-id="9b371-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b371-128">Response</span></span>

<span data-ttu-id="9b371-129">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="9b371-129">If successful, this method returns `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="9b371-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9b371-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9b371-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9b371-131">Request</span></span>
<span data-ttu-id="9b371-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9b371-132">Here is an example of the request.</span></span>
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

<span data-ttu-id="9b371-133">Tenga en cuenta que se necesita dicho encabezado workbook-session-id.</span><span class="sxs-lookup"><span data-stu-id="9b371-133">Note that workbook-session-id header is required.</span></span> 


##### <a name="response"></a><span data-ttu-id="9b371-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b371-134">Response</span></span>
<span data-ttu-id="9b371-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b371-135">Here is an example of the response.</span></span> 

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
    "Warning: close_excel_session//api-reference/v1.0/api/workbook_closesession.md:
      Request includes a non-standard header: workbook-session-id"
  ]
}-->