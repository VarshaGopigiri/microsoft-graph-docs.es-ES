# <a name="get-contactfolder"></a><span data-ttu-id="ea9f4-101">Obtener contactFolder</span><span class="sxs-lookup"><span data-stu-id="ea9f4-101">Get contactFolder</span></span>

<span data-ttu-id="ea9f4-102">Obtiene una carpeta de contactos mediante el id. de carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="ea9f4-102">Get a contact folder by using the contact folder ID.</span></span>

<span data-ttu-id="ea9f4-103">Existen dos casos en los que una aplicación puede obtener la carpeta de contactos de otros usuario:</span><span class="sxs-lookup"><span data-stu-id="ea9f4-103">There are two scenarios where an app can get another user's contact folder:</span></span>

* <span data-ttu-id="ea9f4-104">Si la aplicación tiene permisos de aplicación, o bien,</span><span class="sxs-lookup"><span data-stu-id="ea9f4-104">If the app has application permissions, or,</span></span>
* <span data-ttu-id="ea9f4-105">Si la aplicación tiene [los permisos](#permissions) adecuados de un usuario y otro usuario ha compartido una carpeta de contactos con ese usuario o se le concede acceso delegado a ese usuario.</span><span class="sxs-lookup"><span data-stu-id="ea9f4-105">If the app has the appropriate delegated [permissions](#permissions) from one user, and another user has shared a contact folder with that user, or, has given delegated access to that user.</span></span> <span data-ttu-id="ea9f4-106">Consulte los [detalles y un ejemplo](../../../concepts/outlook-get-shared-contacts-folders.md).</span><span class="sxs-lookup"><span data-stu-id="ea9f4-106">See [details and an example](../../../concepts/outlook-get-shared-contacts-folders.md).</span></span>


## <a name="permissions"></a><span data-ttu-id="ea9f4-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="ea9f4-107">Permissions</span></span>
<span data-ttu-id="ea9f4-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="ea9f4-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="ea9f4-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ea9f4-110">Permission type</span></span>      | <span data-ttu-id="ea9f4-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ea9f4-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ea9f4-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ea9f4-112">Delegated (work or school account)</span></span> | <span data-ttu-id="ea9f4-113">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ea9f4-113">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="ea9f4-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ea9f4-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ea9f4-115">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ea9f4-115">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="ea9f4-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ea9f4-116">Application</span></span> | <span data-ttu-id="ea9f4-117">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ea9f4-117">Contacts.Read, Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="ea9f4-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ea9f4-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/contactFolders/{id}
GET /users/{id | userPrincipalName}/contactFolders/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="ea9f4-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ea9f4-119">Optional query parameters</span></span>
<span data-ttu-id="ea9f4-120">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ea9f4-120">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="ea9f4-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ea9f4-121">Request headers</span></span>
| <span data-ttu-id="ea9f4-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="ea9f4-122">Name</span></span>       | <span data-ttu-id="ea9f4-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="ea9f4-123">Type</span></span> | <span data-ttu-id="ea9f4-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea9f4-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="ea9f4-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="ea9f4-125">Authorization</span></span>  | <span data-ttu-id="ea9f4-126">cadena</span><span class="sxs-lookup"><span data-stu-id="ea9f4-126">string</span></span>  | <span data-ttu-id="ea9f4-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ea9f4-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="ea9f4-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ea9f4-129">Request body</span></span>
<span data-ttu-id="ea9f4-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ea9f4-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ea9f4-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea9f4-131">Response</span></span>

<span data-ttu-id="ea9f4-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [contactFolder](../resources/contactfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ea9f4-132">If successful, this method returns a `200 OK` response code and [contactFolder](../resources/contactfolder.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="ea9f4-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ea9f4-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ea9f4-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ea9f4-134">Request</span></span>
<span data-ttu-id="ea9f4-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ea9f4-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_contactfolder"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/contactFolders/{id}
```
##### <a name="response"></a><span data-ttu-id="ea9f4-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea9f4-136">Response</span></span>
<span data-ttu-id="ea9f4-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ea9f4-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.contactFolder"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 104

{
  "displayName": "Finance",
  "id": "AAMkAGI2TKI5AAA=",
  "parentFolderId": "AAMkAGI2AAEOAAA="
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get contactFolder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
