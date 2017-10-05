# <a name="notebook-getrecentnotebooks"></a><span data-ttu-id="c6dcd-101">notebook: getRecentNotebooks</span><span class="sxs-lookup"><span data-stu-id="c6dcd-101">notebook: getRecentNotebooks</span></span>

<span data-ttu-id="c6dcd-102">Obtener una lista de instancias de [recentNotebook](../resources/recentnotebook.md) a las que ha accedido el usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="c6dcd-102">Get a list of [recentNotebook](../resources/recentnotebook.md) instances that have been accessed by the signed-in user.</span></span>

## <a name="permissions"></a><span data-ttu-id="c6dcd-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="c6dcd-103">Permissions</span></span>
<span data-ttu-id="c6dcd-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="c6dcd-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="c6dcd-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c6dcd-106">Permission type</span></span>      | <span data-ttu-id="c6dcd-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c6dcd-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c6dcd-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c6dcd-108">Delegated (work or school account)</span></span> | <span data-ttu-id="c6dcd-109">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c6dcd-109">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span></span>|
|<span data-ttu-id="c6dcd-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c6dcd-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c6dcd-111">Notes.Create, Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c6dcd-111">Notes.Create, Notes.Read, Notes.ReadWrite</span></span> |
|<span data-ttu-id="c6dcd-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c6dcd-112">Application</span></span> | <span data-ttu-id="c6dcd-113">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c6dcd-113">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="c6dcd-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c6dcd-114">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/notebooks/getRecentNotebooks(includePersonalNotebooks=includePersonalNotebooks-value)
GET /users/<id | userPrincipalName>/onenote/notebooks/getRecentNotebooks(includePersonalNotebooks=includePersonalNotebooks-value)
```

<span data-ttu-id="c6dcd-115">El `<id | userPrincipalName>` del usuario debe coincidir con el usuario codificado en el token de autorización que se usa para realizar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c6dcd-115">The `<id | userPrincipalName>` for the user must match the user encoded in the authorization token used to make the request.</span></span>

## <a name="request-headers"></a><span data-ttu-id="c6dcd-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c6dcd-116">Request headers</span></span>
| <span data-ttu-id="c6dcd-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="c6dcd-117">Name</span></span>       | <span data-ttu-id="c6dcd-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="c6dcd-118">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="c6dcd-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="c6dcd-119">Authorization</span></span>  | <span data-ttu-id="c6dcd-120">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="c6dcd-120">Bearer {code}</span></span>|

## <a name="request-parameters"></a><span data-ttu-id="c6dcd-121">Parámetros de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c6dcd-121">Request parameters</span></span>
<span data-ttu-id="c6dcd-122">En la dirección URL de la solicitud, especifique los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="c6dcd-122">In the request URL, provide following query parameters with values.</span></span>

| <span data-ttu-id="c6dcd-123">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c6dcd-123">Parameter</span></span>    | <span data-ttu-id="c6dcd-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="c6dcd-124">Type</span></span>   |<span data-ttu-id="c6dcd-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="c6dcd-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c6dcd-126">includePersonalNotebooks</span><span class="sxs-lookup"><span data-stu-id="c6dcd-126">includePersonalNotebooks</span></span>|<span data-ttu-id="c6dcd-127">Boolean</span><span class="sxs-lookup"><span data-stu-id="c6dcd-127">Boolean</span></span>|<span data-ttu-id="c6dcd-128">Incluir los blocs de notas que pertenecen al usuario.</span><span class="sxs-lookup"><span data-stu-id="c6dcd-128">Include notebooks owned by the user.</span></span> <span data-ttu-id="c6dcd-129">Se establece en `true` para incluir los blocs de notas que pertenecen al usuario; en caso contrario, se establece en `false`.</span><span class="sxs-lookup"><span data-stu-id="c6dcd-129">Set to `true` to include notebooks owned by the user; otherwise, set to `false`.</span></span> <span data-ttu-id="c6dcd-130">Si no incluye el parámetro `includePersonalNotebooks`, la solicitud devolverá una respuesta de error `400`.</span><span class="sxs-lookup"><span data-stu-id="c6dcd-130">If you don't include the `includePersonalNotebooks` parameter, your request will return a `400` error response.</span></span>|

## <a name="request-body"></a><span data-ttu-id="c6dcd-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c6dcd-131">Request body</span></span>
<span data-ttu-id="c6dcd-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c6dcd-132">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c6dcd-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c6dcd-133">Response</span></span>
<span data-ttu-id="c6dcd-134">Una respuesta correcta devuelve un valor `200 OK` que contiene una colección JSON de **recentNotebooks**.</span><span class="sxs-lookup"><span data-stu-id="c6dcd-134">A successful response returns a `200 OK` that contains a JSON collection of **recentNotebooks**.</span></span>

## <a name="example"></a><span data-ttu-id="c6dcd-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c6dcd-135">Example</span></span>
<span data-ttu-id="c6dcd-136">En el siguiente ejemplo se muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="c6dcd-136">The following example shows how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="c6dcd-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c6dcd-137">Request</span></span>
<span data-ttu-id="c6dcd-138">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c6dcd-138">The following example shows the request.</span></span>
<!-- { "blockType": "request", "name": "recent_notebooks", "scopes": "notes.read" } -->
```http
GET https://graph.microsoft.com/v1.0/onenote/notebooks/getrecentnotebooks(includePersonalNotebooks=true)
```

#### <a name="response"></a><span data-ttu-id="c6dcd-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c6dcd-139">Response</span></span>
<span data-ttu-id="c6dcd-140">En el ejemplo siguiente se muestra la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c6dcd-140">The following example shows the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.notebook",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-Length: 1110

{
  "value":[
    {
      "name":"Personal Notebook","lastAccessedTime":"timestamp","links":{
        "oneNoteClientUrl":{
          "href":"onenote:href-value"
        },"oneNoteWebUrl":{
          "href":"href-value"
        }
      },"sourceService":"OneDrive"
    },{
      "name":"Team Shared Notebook","lastAccessedTime":"timestamp","links":{
        "oneNoteClientUrl":{
          "href":"onenote:href-value"
        },"oneNoteWebUrl":{
          "href":"href-value"
        }
      },"sourceService":"OneDriveForBusiness"
    }
  ]
}
```
