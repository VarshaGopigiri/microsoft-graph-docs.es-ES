# <a name="notebook-getrecentnotebooks"></a><span data-ttu-id="76f0e-101">notebook: getRecentNotebooks</span><span class="sxs-lookup"><span data-stu-id="76f0e-101">notebook: getRecentNotebooks</span></span>

<span data-ttu-id="76f0e-102">Obtener una lista de instancias de [recentNotebook](../resources/recentnotebook.md) a las que ha accedido el usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="76f0e-102">Get a list of [recentNotebook](../resources/recentnotebook.md) instances that have been accessed by the signed-in user.</span></span>

## <a name="permissions"></a><span data-ttu-id="76f0e-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="76f0e-103">Permissions</span></span>
<span data-ttu-id="76f0e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="76f0e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="76f0e-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="76f0e-106">Permission type</span></span>      | <span data-ttu-id="76f0e-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="76f0e-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="76f0e-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="76f0e-108">Delegated (work or school account)</span></span> | <span data-ttu-id="76f0e-109">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="76f0e-109">Notes.Create, Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All,</span></span>|
|<span data-ttu-id="76f0e-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="76f0e-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="76f0e-111">Notes.Create, Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="76f0e-111">Notes.Create, Notes.Read, Notes.ReadWrite</span></span> |
|<span data-ttu-id="76f0e-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="76f0e-112">Application</span></span> | <span data-ttu-id="76f0e-113">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="76f0e-113">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="76f0e-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="76f0e-114">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/notebooks/getRecentNotebooks(includePersonalNotebooks=includePersonalNotebooks-value)
GET /users/{id | userPrincipalName}/onenote/notebooks/getRecentNotebooks(includePersonalNotebooks=includePersonalNotebooks-value)
```

<span data-ttu-id="76f0e-115">El `<id | userPrincipalName>` del usuario debe coincidir con el usuario codificado en el token de autorización que se usa para realizar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="76f0e-115">The `<id | userPrincipalName>` for the user must match the user encoded in the authorization token used to make the request.</span></span>

## <a name="function-parameters"></a><span data-ttu-id="76f0e-116">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="76f0e-116">Function parameters</span></span>

| <span data-ttu-id="76f0e-117">Parámetro</span><span class="sxs-lookup"><span data-stu-id="76f0e-117">Parameter</span></span>    | <span data-ttu-id="76f0e-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="76f0e-118">Type</span></span>   |<span data-ttu-id="76f0e-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="76f0e-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="76f0e-120">includePersonalNotebooks</span><span class="sxs-lookup"><span data-stu-id="76f0e-120">includePersonalNotebooks</span></span>|<span data-ttu-id="76f0e-121">Booleano</span><span class="sxs-lookup"><span data-stu-id="76f0e-121">Boolean</span></span>|<span data-ttu-id="76f0e-122">Incluir los blocs de notas que pertenecen al usuario.</span><span class="sxs-lookup"><span data-stu-id="76f0e-122">Include notebooks owned by the user.</span></span> <span data-ttu-id="76f0e-123">Se establece en `true` para incluir los blocs de notas que pertenecen al usuario; en caso contrario, se establece en `false`.</span><span class="sxs-lookup"><span data-stu-id="76f0e-123">Set to `true` to include notebooks owned by the user; otherwise, set to `false`.</span></span> <span data-ttu-id="76f0e-124">Si no incluye el parámetro `includePersonalNotebooks`, la solicitud devolverá una respuesta de error `400`.</span><span class="sxs-lookup"><span data-stu-id="76f0e-124">If you don't include the `includePersonalNotebooks` parameter, your request will return a `400` error response.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="76f0e-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="76f0e-125">Request headers</span></span>
| <span data-ttu-id="76f0e-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="76f0e-126">Name</span></span>       | <span data-ttu-id="76f0e-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="76f0e-127">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="76f0e-128">Autorización</span><span class="sxs-lookup"><span data-stu-id="76f0e-128">Authorization</span></span>  | <span data-ttu-id="76f0e-129">Portador {código}</span><span class="sxs-lookup"><span data-stu-id="76f0e-129">Bearer {code}</span></span>|

## <a name="request-body"></a><span data-ttu-id="76f0e-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="76f0e-130">Request body</span></span>
<span data-ttu-id="76f0e-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="76f0e-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="76f0e-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="76f0e-132">Response</span></span>
<span data-ttu-id="76f0e-133">Una respuesta correcta devuelve un valor `200 OK` que contiene una colección JSON de **recentNotebooks**.</span><span class="sxs-lookup"><span data-stu-id="76f0e-133">A successful response returns a `200 OK` that contains a JSON collection of **recentNotebooks**.</span></span>

## <a name="example"></a><span data-ttu-id="76f0e-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="76f0e-134">Example</span></span>
<span data-ttu-id="76f0e-135">En el siguiente ejemplo se muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="76f0e-135">The following example shows how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="76f0e-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="76f0e-136">Request</span></span>
<span data-ttu-id="76f0e-137">En el ejemplo siguiente se muestra la solicitud.</span><span class="sxs-lookup"><span data-stu-id="76f0e-137">The following example shows the request.</span></span>
<!-- { "blockType": "request", "name": "recent_notebooks", "scopes": "notes.read" } -->
```http
GET https://graph.microsoft.com/v1.0/me/onenote/notebooks/getRecentNotebooks(includePersonalNotebooks=true)
```

#### <a name="response"></a><span data-ttu-id="76f0e-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="76f0e-138">Response</span></span>
<span data-ttu-id="76f0e-139">En el ejemplo siguiente se muestra la respuesta.</span><span class="sxs-lookup"><span data-stu-id="76f0e-139">The following example shows the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.recentNotebook)",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-Length: 1110

{
  "value":[
    {
      "displayName":"Personal Notebook","lastAccessedTime":"timestamp","links":{
        "oneNoteClientUrl":{
          "href":"onenote:href-value"
        },"oneNoteWebUrl":{
          "href":"href-value"
        }
      },"sourceService":"OneDrive"
    },{
      "displayName":"Team Shared Notebook","lastAccessedTime":"timestamp","links":{
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
