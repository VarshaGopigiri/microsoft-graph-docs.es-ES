# <a name="get-drive"></a><span data-ttu-id="f8f2d-101">Obtener unidad</span><span class="sxs-lookup"><span data-stu-id="f8f2d-101">Get Drive</span></span>

<span data-ttu-id="f8f2d-p101">Recupere las propiedades y relaciones de un recurso [Drive](../resources/drive.md). Un recurso Drive es el contenedor de nivel superior de un sistema de archivos. La API Graph le permite acceder al recurso Drive de las bibliotecas de documentos de OneDrive, OneDrive para la Empresa o SharePoint de un usuario.</span><span class="sxs-lookup"><span data-stu-id="f8f2d-p101">Retrieve the properties and relationships of a [Drive](../resources/drive.md) resource. A Drive is the top-level container for a file system. Graph API allows access to the Drive resource for a user's OneDrive or OneDrive for Business, or SharePoint document libraries.</span></span>

## <a name="permissions"></a><span data-ttu-id="f8f2d-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="f8f2d-105">Permissions</span></span>

<span data-ttu-id="f8f2d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="f8f2d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="f8f2d-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f8f2d-108">Permission type</span></span>      | <span data-ttu-id="f8f2d-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f8f2d-109">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="f8f2d-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f8f2d-110">Delegated (work or school account)</span></span> | <span data-ttu-id="f8f2d-111">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f8f2d-111">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    | 
|<span data-ttu-id="f8f2d-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f8f2d-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f8f2d-113">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f8f2d-113">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    | 
|<span data-ttu-id="f8f2d-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f8f2d-114">Application</span></span> | <span data-ttu-id="f8f2d-115">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f8f2d-115">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> | 

## <a name="get-a-users-onedrive"></a><span data-ttu-id="f8f2d-116">Obtener la cuenta de OneDrive de un usuario</span><span class="sxs-lookup"><span data-stu-id="f8f2d-116">Get a user's OneDrive</span></span>

<span data-ttu-id="f8f2d-117">Para acceder al OneDrive o OneDrive para la Empresa de un usuario, la aplicación debe solicitar la relación **drive** en el recurso [User](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="f8f2d-117">To access a user's OneDrive or OneDrive for Business, your app must request the **drive** relationship on the [User](../resources/user.md) resource.</span></span>

## <a name="http-request"></a><span data-ttu-id="f8f2d-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f8f2d-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /me/drive
GET /users/{idOrUserPrincipalName}/drive
```

## <a name="get-the-document-library-associated-with-a-group"></a><span data-ttu-id="f8f2d-119">Obtener la biblioteca de documentos asociada a un grupo</span><span class="sxs-lookup"><span data-stu-id="f8f2d-119">Get the document library associated with a group</span></span>

<span data-ttu-id="f8f2d-120">Para acceder a la biblioteca de documentos predeterminada de un [grupo](../resources/group.md), la aplicación solicita la relación **drive** en el grupo.</span><span class="sxs-lookup"><span data-stu-id="f8f2d-120">To access a [Group's](../resources/group.md) default document library, your app requests the **drive** relationship on the Group.</span></span>

## <a name="http-request"></a><span data-ttu-id="f8f2d-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f8f2d-121">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /groups/{idOrUserPrincipalName}/drive
```


## <a name="optional-query-parameters"></a><span data-ttu-id="f8f2d-122">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="f8f2d-122">Optional query parameters</span></span>

<span data-ttu-id="f8f2d-123">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f8f2d-123">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-body"></a><span data-ttu-id="f8f2d-124">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="f8f2d-124">Request body</span></span>

<span data-ttu-id="f8f2d-125">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f8f2d-125">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f8f2d-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f8f2d-126">Response</span></span>

<span data-ttu-id="f8f2d-127">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el recurso [Drive](../resources/drive.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f8f2d-127">If successful, this method returns a `200 OK` response code and [Drive](../resources/drive.md) resource in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f8f2d-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f8f2d-128">Example</span></span>

##### <a name="request"></a><span data-ttu-id="f8f2d-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f8f2d-129">Request</span></span>

<span data-ttu-id="f8f2d-130">Este es un ejemplo de la solicitud para obtener el OneDrive o OneDrive para la Empresa del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="f8f2d-130">Here is an example of the request to get the sign-in user's OneDrive or OneDrive for Business.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_drive"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive
```

##### <a name="response"></a><span data-ttu-id="f8f2d-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f8f2d-131">Response</span></span>

<span data-ttu-id="f8f2d-132">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f8f2d-132">Here is an example of the response.</span></span>

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
