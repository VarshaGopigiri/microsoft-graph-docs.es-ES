# <a name="get-contactfolder"></a><span data-ttu-id="83a28-101">Get contactFolder</span><span class="sxs-lookup"><span data-stu-id="83a28-101">Get contactFolder</span></span>

<span data-ttu-id="83a28-102">Obtiene una carpeta de contactos mediante el id. de carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="83a28-102">Get a contact folder by using the contact folder ID.</span></span>
## <a name="permissions"></a><span data-ttu-id="83a28-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="83a28-103">Permissions</span></span>
<span data-ttu-id="83a28-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="83a28-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="83a28-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="83a28-106">Permission type</span></span>      | <span data-ttu-id="83a28-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="83a28-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="83a28-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="83a28-108">Delegated (work or school account)</span></span> | <span data-ttu-id="83a28-109">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="83a28-109">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="83a28-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="83a28-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="83a28-111">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="83a28-111">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="83a28-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="83a28-112">Application</span></span> | <span data-ttu-id="83a28-113">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="83a28-113">Contacts.Read, Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="83a28-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="83a28-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/contactFolders/{id}
GET /users/{id | userPrincipalName}/contactFolders/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="83a28-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="83a28-115">Optional query parameters</span></span>
<span data-ttu-id="83a28-116">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="83a28-116">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="83a28-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="83a28-117">Request headers</span></span>
| <span data-ttu-id="83a28-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="83a28-118">Name</span></span>       | <span data-ttu-id="83a28-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="83a28-119">Type</span></span> | <span data-ttu-id="83a28-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="83a28-120">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="83a28-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="83a28-121">Authorization</span></span>  | <span data-ttu-id="83a28-122">string</span><span class="sxs-lookup"><span data-stu-id="83a28-122">string</span></span>  | <span data-ttu-id="83a28-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="83a28-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="83a28-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="83a28-125">Request body</span></span>
<span data-ttu-id="83a28-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="83a28-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="83a28-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="83a28-127">Response</span></span>

<span data-ttu-id="83a28-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [contactFolder](../resources/contactfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="83a28-128">If successful, this method returns a `200 OK` response code and [contactFolder](../resources/contactfolder.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="83a28-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="83a28-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="83a28-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="83a28-130">Request</span></span>
<span data-ttu-id="83a28-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="83a28-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_contactfolder"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/contactFolders/{id}
```
##### <a name="response"></a><span data-ttu-id="83a28-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="83a28-132">Response</span></span>
<span data-ttu-id="83a28-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="83a28-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
