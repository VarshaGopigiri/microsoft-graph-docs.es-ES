<span data-ttu-id="93af1-p101">Recupere las propiedades y relaciones de un recurso [Drive](../resources/drive.md). Un recurso Drive es el contenedor de nivel superior de un sistema de archivos. La API Graph le permite acceder al recurso Drive de las bibliotecas de documentos de OneDrive, OneDrive para la Empresa o SharePoint de un usuario.</span><span class="sxs-lookup"><span data-stu-id="93af1-p101">Retrieve the properties and relationships of a [Drive](../resources/drive.md) resource. A Drive is the top-level container for a file system. Graph API allows access to the Drive resource for a user's OneDrive or OneDrive for Business, or SharePoint document libraries.</span></span>

Recupere las propiedades y relaciones de un recurso [Drive](../resources/drive.md). Un recurso Drive es el contenedor de nivel superior de un sistema de archivos. La API Graph le permite acceder al recurso Drive de las bibliotecas de documentos de OneDrive, OneDrive para la Empresa o SharePoint de un usuario.

## <span data-ttu-id="93af1-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="93af1-105">Prerequisites</span></span>
<a id="prerequisites" class="xliff"></a>

<span data-ttu-id="93af1-106">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="93af1-106">One of the following **scopes** is required to execute this API:</span></span>

* <span data-ttu-id="93af1-107">Files.Read</span><span class="sxs-lookup"><span data-stu-id="93af1-107">Files.Read</span></span>
* <span data-ttu-id="93af1-108">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="93af1-108">Files.ReadWrite</span></span>
* <span data-ttu-id="93af1-109">Files.Read.All</span><span class="sxs-lookup"><span data-stu-id="93af1-109">Files.Read.All</span></span>
* <span data-ttu-id="93af1-110">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="93af1-110">Files.ReadWrite.All</span></span>
* <span data-ttu-id="93af1-111">Sites.Read.All</span><span class="sxs-lookup"><span data-stu-id="93af1-111">Sites.Read.All</span></span>
* <span data-ttu-id="93af1-112">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="93af1-112">Sites.ReadWrite.All</span></span>

## <span data-ttu-id="93af1-113">Obtener la cuenta de OneDrive de un usuario</span><span class="sxs-lookup"><span data-stu-id="93af1-113">Get a user's OneDrive</span></span>
<a id="get-a-users-onedrive" class="xliff"></a>

<span data-ttu-id="93af1-114">Para acceder al OneDrive o OneDrive para la Empresa de un usuario, la aplicación debe solicitar la relación **drive** en el recurso [User](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="93af1-114">To access a user's OneDrive or OneDrive for Business, your app must request the **drive** relationship on the [User](../resources/user.md) resource.</span></span>

### <span data-ttu-id="93af1-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="93af1-115">HTTP request</span></span>
<a id="http-request" class="xliff"></a>

<!-- { "blockType": "ignored" } -->

```http
GET /me/drive
GET /users/{idOrUserPrincipalName}/drive
```

## <span data-ttu-id="93af1-116">Obtener la biblioteca de documentos asociada a un grupo</span><span class="sxs-lookup"><span data-stu-id="93af1-116">Get the document library associated with a group</span></span>
<a id="get-the-document-library-associated-with-a-group" class="xliff"></a>

<span data-ttu-id="93af1-117">Para acceder a la biblioteca de documentos predeterminada de un [grupo](../resources/group.md), la aplicación solicita la relación **drive** en el grupo.</span><span class="sxs-lookup"><span data-stu-id="93af1-117">To access a [Group's](../resources/group.md) default document library, your app requests the **drive** relationship on the Group.</span></span>

### <span data-ttu-id="93af1-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="93af1-118">HTTP request</span></span>
<a id="http-request" class="xliff"></a>

<!-- { "blockType": "ignored" } -->

```http
GET /groups/{idOrUserPrincipalName}/drive
```


## <span data-ttu-id="93af1-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="93af1-119">Optional query parameters</span></span>
<a id="optional-query-parameters" class="xliff"></a>

<span data-ttu-id="93af1-120">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="93af1-120">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

## <span data-ttu-id="93af1-121">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="93af1-121">Request body</span></span>
<a id="request-body" class="xliff"></a>

<span data-ttu-id="93af1-122">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="93af1-122">Do not supply a request body for this method.</span></span>

## <span data-ttu-id="93af1-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="93af1-123">Response</span></span>
<a id="response" class="xliff"></a>

<span data-ttu-id="93af1-124">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el recurso [Drive](../resources/drive.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="93af1-124">If successful, this method returns a `200 OK` response code and [Drive](../resources/drive.md) resource in the response body.</span></span>

## <span data-ttu-id="93af1-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="93af1-125">Example</span></span>
<a id="example" class="xliff"></a>

##### <span data-ttu-id="93af1-126">Solicitud</span><span class="sxs-lookup"><span data-stu-id="93af1-126">Request</span></span>
<a id="request" class="xliff"></a>

<span data-ttu-id="93af1-127">Este es un ejemplo de la solicitud para obtener el OneDrive o OneDrive para la Empresa del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="93af1-127">Here is an example of the request to get the sign-in user's OneDrive or OneDrive for Business.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_drive"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive
```

##### <span data-ttu-id="93af1-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="93af1-128">Response</span></span>
<a id="response" class="xliff"></a>

<span data-ttu-id="93af1-129">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="93af1-129">Here is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.drive"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "id": "b!t18F8ybsHUq1z3LTz8xvZqP8zaSWjkFNhsME-Fepo75dTf9vQKfeRblBZjoSQrd7",
    "driveType": "business",    
    "owner": {
        "user": {
            "id": "efee1b77-fb3b-4f65-99d6-274c11914d12",
            "displayName": "Ryan Gregg"
        }
    },
    "quota": {
        "deleted": 256938,
        "remaining": 1099447353539,
        "state": "normal",
        "total": 1099511627776
    }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get metadata for a OneDrive, OneDrive for Business, or Office 365 group drive",
  "keywords": "drive,onedrive,default drive,group drive",
  "section": "documentation",
  "tocPath": "OneDrive/Drive/Get Drive"
}-->
