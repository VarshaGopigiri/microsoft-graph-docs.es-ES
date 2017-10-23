# <a name="mailfolder-copy"></a><span data-ttu-id="f34e9-101">mailFolder: copy</span><span class="sxs-lookup"><span data-stu-id="f34e9-101">mailFolder: copy</span></span>

<span data-ttu-id="f34e9-102">Copia un objeto mailfolder y su contenido en otro objeto mailfolder.</span><span class="sxs-lookup"><span data-stu-id="f34e9-102">Copy a mailfolder and its contents to another mailfolder.</span></span>

## <a name="permissions"></a><span data-ttu-id="f34e9-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="f34e9-103">Permissions</span></span>
<span data-ttu-id="f34e9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="f34e9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="f34e9-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f34e9-106">Permission type</span></span>      | <span data-ttu-id="f34e9-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f34e9-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f34e9-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f34e9-108">Delegated (work or school account)</span></span> | <span data-ttu-id="f34e9-109">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f34e9-109">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="f34e9-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f34e9-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f34e9-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f34e9-111">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="f34e9-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f34e9-112">Application</span></span> | <span data-ttu-id="f34e9-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f34e9-113">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="f34e9-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f34e9-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/mailFolders/{id}/copy
POST /users/{id | userPrincipalName}/mailFolders/{id}/copy
```
## <a name="request-headers"></a><span data-ttu-id="f34e9-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f34e9-115">Request headers</span></span>
| <span data-ttu-id="f34e9-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f34e9-116">Header</span></span>       | <span data-ttu-id="f34e9-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f34e9-117">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="f34e9-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="f34e9-118">Authorization</span></span>  | <span data-ttu-id="f34e9-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f34e9-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="f34e9-121">Content-Type</span><span class="sxs-lookup"><span data-stu-id="f34e9-121">Content-Type</span></span>  | <span data-ttu-id="f34e9-p103">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f34e9-p103">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="f34e9-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f34e9-124">Request body</span></span>
<span data-ttu-id="f34e9-125">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="f34e9-125">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="f34e9-126">Parámetro</span><span class="sxs-lookup"><span data-stu-id="f34e9-126">Parameter</span></span>    | <span data-ttu-id="f34e9-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="f34e9-127">Type</span></span>   |<span data-ttu-id="f34e9-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="f34e9-128">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f34e9-129">destinationId</span><span class="sxs-lookup"><span data-stu-id="f34e9-129">destinationId</span></span>|<span data-ttu-id="f34e9-130">String</span><span class="sxs-lookup"><span data-stu-id="f34e9-130">String</span></span>|<span data-ttu-id="f34e9-131">Identificador de la carpeta o el nombre de carpeta conocido *Inbox*, *Drafts*, *SentItems* o *DeletedItems*.</span><span class="sxs-lookup"><span data-stu-id="f34e9-131">The folder ID, or the *Inbox*, *Drafts*, *SentItems*, or *DeletedItems* well-known folder name.</span></span>|

## <a name="response"></a><span data-ttu-id="f34e9-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f34e9-132">Response</span></span>

<span data-ttu-id="f34e9-133">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [MailFolder](../resources/mailfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f34e9-133">If successful, this method returns `200 OK` response code and [MailFolder](../resources/mailfolder.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f34e9-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f34e9-134">Example</span></span>
<span data-ttu-id="f34e9-135">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="f34e9-135">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="f34e9-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f34e9-136">Request</span></span>
<span data-ttu-id="f34e9-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f34e9-137">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "mailfolder_copy"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/mailFolders/{id}/copy
Content-type: application/json
Content-length: 44

{
  "destinationId": "destinationId-value"
}
```

##### <a name="response"></a><span data-ttu-id="f34e9-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f34e9-138">Response</span></span>
<span data-ttu-id="f34e9-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f34e9-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "mailFolder: copy",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
