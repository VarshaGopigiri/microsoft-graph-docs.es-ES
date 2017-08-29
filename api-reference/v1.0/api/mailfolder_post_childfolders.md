# <a name="create-mailfolder"></a><span data-ttu-id="67250-101">Create MailFolder</span><span class="sxs-lookup"><span data-stu-id="67250-101">Create MailFolder</span></span>

<span data-ttu-id="67250-102">Use esta API para crear un objeto mailfolder secundario.</span><span class="sxs-lookup"><span data-stu-id="67250-102">Use this API to create a new child mailfolder.</span></span>

## <a name="permissions"></a><span data-ttu-id="67250-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="67250-103">Permissions</span></span>
<span data-ttu-id="67250-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="67250-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="67250-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="67250-106">Permission type</span></span>      | <span data-ttu-id="67250-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="67250-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="67250-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="67250-108">Delegated (work or school account)</span></span> | <span data-ttu-id="67250-109">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="67250-109">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="67250-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="67250-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="67250-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="67250-111">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="67250-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="67250-112">Application</span></span> | <span data-ttu-id="67250-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="67250-113">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="67250-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="67250-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/mailFolders/{id}/childFolders
POST /users/{id | userPrincipalName}/mailFolders/{id}/childFolders
```

<span data-ttu-id="67250-115">Especifique la carpeta principal en la dirección URL de consulta como identificador de la carpeta o el nombre de carpeta conocido `Inbox`, `Drafts`, `SentItems` o `DeletedItems`.</span><span class="sxs-lookup"><span data-stu-id="67250-115">Specify the parent folder in the query URL as a folder ID, or the `Inbox`, `Drafts`, `SentItems`, or `DeletedItems` well-known folder name.</span></span>

## <a name="request-headers"></a><span data-ttu-id="67250-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="67250-116">Request headers</span></span>
| <span data-ttu-id="67250-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="67250-117">Header</span></span>       | <span data-ttu-id="67250-118">Valor</span><span class="sxs-lookup"><span data-stu-id="67250-118">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="67250-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="67250-119">Authorization</span></span>  | <span data-ttu-id="67250-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="67250-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="67250-122">Content-Type</span><span class="sxs-lookup"><span data-stu-id="67250-122">Content-Type</span></span>  | <span data-ttu-id="67250-p103">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="67250-p103">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="67250-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="67250-125">Request body</span></span>
<span data-ttu-id="67250-p104">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros. **displayName** es la única propiedad que se puede escribir de un objeto [MailFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="67250-p104">In the request body, provide a JSON object with the following parameters. **displayName** is the only writable property for a [MailFolder](../resources/mailfolder.md) object.</span></span>

| <span data-ttu-id="67250-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="67250-128">Parameter</span></span>    | <span data-ttu-id="67250-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="67250-129">Type</span></span>   |<span data-ttu-id="67250-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="67250-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="67250-131">displayName</span><span class="sxs-lookup"><span data-stu-id="67250-131">displayName</span></span>|<span data-ttu-id="67250-132">String</span><span class="sxs-lookup"><span data-stu-id="67250-132">String</span></span>|<span data-ttu-id="67250-133">Nombre para mostrar de la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="67250-133">The display name of the new folder.</span></span>|

## <a name="response"></a><span data-ttu-id="67250-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="67250-134">Response</span></span>

<span data-ttu-id="67250-135">Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y el objeto [MailFolder](../resources/mailfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="67250-135">If successful, this method returns `201, Created` response code and [MailFolder](../resources/mailfolder.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="67250-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="67250-136">Example</span></span>
##### <a name="request"></a><span data-ttu-id="67250-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="67250-137">Request</span></span>
<span data-ttu-id="67250-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="67250-138">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_mailfolder_from_mailfolder"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/mailFolders/{id}/childFolders
Content-type: application/json
Content-length: 159

{
  "displayName": "displayName-value",
}
```

##### <a name="response"></a><span data-ttu-id="67250-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="67250-139">Response</span></span>
<span data-ttu-id="67250-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="67250-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Create MailFolder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
