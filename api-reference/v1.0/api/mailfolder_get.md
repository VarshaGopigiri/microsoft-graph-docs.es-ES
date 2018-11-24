# <a name="get-mailfolder"></a><span data-ttu-id="beab5-101">Get mailFolder</span><span class="sxs-lookup"><span data-stu-id="beab5-101">Get mailFolder</span></span>

<span data-ttu-id="beab5-102">Recupere las propiedades y las relaciones de un objeto de carpeta de mensajes.</span><span class="sxs-lookup"><span data-stu-id="beab5-102">Retrieve the properties and relationships of a message folder object.</span></span>

<span data-ttu-id="beab5-103">Hay dos escenarios donde una aplicación puede obtener la carpeta de correo de otro usuario:</span><span class="sxs-lookup"><span data-stu-id="beab5-103">There are two scenarios where an app can get another user's mail folder:</span></span>

* <span data-ttu-id="beab5-104">Si la aplicación tiene permisos de aplicación, o bien,</span><span class="sxs-lookup"><span data-stu-id="beab5-104">If the app has application permissions, or,</span></span>
* <span data-ttu-id="beab5-105">Si la aplicación tiene la adecuada delega [los permisos](#permissions) de un usuario y otro usuario ha compartido una carpeta de correo con ese usuario o, se le concede acceso delegado a ese usuario.</span><span class="sxs-lookup"><span data-stu-id="beab5-105">If the app has the appropriate delegated [permissions](#permissions) from one user, and another user has shared a mail folder with that user, or, has given delegated access to that user.</span></span> <span data-ttu-id="beab5-106">Consulte los [Detalles y un ejemplo](../../../concepts/outlook-share-messages-folders.md).</span><span class="sxs-lookup"><span data-stu-id="beab5-106">See [details and an example](../../../concepts/outlook-share-messages-folders.md).</span></span>


## <a name="permissions"></a><span data-ttu-id="beab5-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="beab5-107">Permissions</span></span>
<span data-ttu-id="beab5-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="beab5-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="beab5-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="beab5-110">Permission type</span></span>      | <span data-ttu-id="beab5-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="beab5-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="beab5-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="beab5-112">Delegated (work or school account)</span></span> | <span data-ttu-id="beab5-113">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="beab5-113">Mail.Read, Mail.ReadWrite</span></span>    |
|<span data-ttu-id="beab5-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="beab5-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="beab5-115">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="beab5-115">Mail.Read, Mail.ReadWrite</span></span>    |
|<span data-ttu-id="beab5-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="beab5-116">Application</span></span> | <span data-ttu-id="beab5-117">Mail.Read, Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="beab5-117">Mail.Read, Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="beab5-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="beab5-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/mailFolders/{id}
GET /users/{id | userPrincipalName}/mailFolders/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="beab5-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="beab5-119">Optional query parameters</span></span>
<span data-ttu-id="beab5-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="beab5-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="beab5-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="beab5-121">Request headers</span></span>
| <span data-ttu-id="beab5-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="beab5-122">Name</span></span>       | <span data-ttu-id="beab5-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="beab5-123">Type</span></span> | <span data-ttu-id="beab5-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="beab5-124">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="beab5-125">Authorization</span><span class="sxs-lookup"><span data-stu-id="beab5-125">Authorization</span></span>  | <span data-ttu-id="beab5-126">string</span><span class="sxs-lookup"><span data-stu-id="beab5-126">string</span></span>  | <span data-ttu-id="beab5-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="beab5-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="beab5-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="beab5-129">Request body</span></span>
<span data-ttu-id="beab5-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="beab5-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="beab5-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="beab5-131">Response</span></span>

<span data-ttu-id="beab5-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [mailFolder](../resources/mailfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="beab5-132">If successful, this method returns a `200 OK` response code and [mailFolder](../resources/mailfolder.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="beab5-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="beab5-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="beab5-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="beab5-134">Request</span></span>
<span data-ttu-id="beab5-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="beab5-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_mailfolder"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/mailFolders/{id}
```
##### <a name="response"></a><span data-ttu-id="beab5-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="beab5-136">Response</span></span>
<span data-ttu-id="beab5-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="beab5-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.mailFolder"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 179

{
  "displayName": "displayName-value",
  "parentFolderId": "parentFolderId-value",
  "childFolderCount": 99,
  "unreadItemCount": 99,
  "totalItemCount": 99,
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get mailFolder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
