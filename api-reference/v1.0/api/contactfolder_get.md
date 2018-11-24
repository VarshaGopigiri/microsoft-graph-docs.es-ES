# <a name="get-contactfolder"></a><span data-ttu-id="88767-101">Get contactFolder</span><span class="sxs-lookup"><span data-stu-id="88767-101">Get contactFolder</span></span>

<span data-ttu-id="88767-102">Obtiene una carpeta de contactos mediante el id. de carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="88767-102">Get a contact folder by using the contact folder ID.</span></span>

<span data-ttu-id="88767-103">Hay dos escenarios donde una aplicación puede obtener la carpeta de contactos de otro usuario:</span><span class="sxs-lookup"><span data-stu-id="88767-103">There are two scenarios where an app can get another user's contact folder:</span></span>

* <span data-ttu-id="88767-104">Si la aplicación tiene permisos de aplicación, o bien,</span><span class="sxs-lookup"><span data-stu-id="88767-104">If the app has application permissions, or,</span></span>
* <span data-ttu-id="88767-105">Si la aplicación tiene la adecuada delega [los permisos](#permissions) de un usuario y otro usuario ha compartido una carpeta de contactos con ese usuario o, se le concede acceso delegado a ese usuario.</span><span class="sxs-lookup"><span data-stu-id="88767-105">If the app has the appropriate delegated [permissions](#permissions) from one user, and another user has shared a contact folder with that user, or, has given delegated access to that user.</span></span> <span data-ttu-id="88767-106">Consulte los [Detalles y un ejemplo](../../../concepts/outlook-get-shared-contacts-folders.md).</span><span class="sxs-lookup"><span data-stu-id="88767-106">See [details and an example](../../../concepts/outlook-get-shared-contacts-folders.md).</span></span>


## <a name="permissions"></a><span data-ttu-id="88767-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="88767-107">Permissions</span></span>
<span data-ttu-id="88767-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="88767-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="88767-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="88767-110">Permission type</span></span>      | <span data-ttu-id="88767-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="88767-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="88767-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="88767-112">Delegated (work or school account)</span></span> | <span data-ttu-id="88767-113">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="88767-113">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="88767-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="88767-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="88767-115">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="88767-115">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="88767-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="88767-116">Application</span></span> | <span data-ttu-id="88767-117">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="88767-117">Contacts.Read, Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="88767-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="88767-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/contactFolders/{id}
GET /users/{id | userPrincipalName}/contactFolders/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="88767-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="88767-119">Optional query parameters</span></span>
<span data-ttu-id="88767-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="88767-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="88767-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="88767-121">Request headers</span></span>
| <span data-ttu-id="88767-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="88767-122">Name</span></span>       | <span data-ttu-id="88767-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="88767-123">Type</span></span> | <span data-ttu-id="88767-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="88767-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="88767-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="88767-125">Authorization</span></span>  | <span data-ttu-id="88767-126">string</span><span class="sxs-lookup"><span data-stu-id="88767-126">string</span></span>  | <span data-ttu-id="88767-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="88767-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="88767-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="88767-129">Request body</span></span>
<span data-ttu-id="88767-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="88767-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="88767-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="88767-131">Response</span></span>

<span data-ttu-id="88767-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [contactFolder](../resources/contactfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="88767-132">If successful, this method returns a `200 OK` response code and [contactFolder](../resources/contactfolder.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="88767-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="88767-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="88767-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="88767-134">Request</span></span>
<span data-ttu-id="88767-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="88767-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_contactfolder"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/contactFolders/{id}
```
##### <a name="response"></a><span data-ttu-id="88767-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="88767-136">Response</span></span>
<span data-ttu-id="88767-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="88767-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
