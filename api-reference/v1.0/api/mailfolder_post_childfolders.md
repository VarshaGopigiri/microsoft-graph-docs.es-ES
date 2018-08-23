# <a name="create-mailfolder"></a><span data-ttu-id="278e2-101">Crear MailFolder</span><span class="sxs-lookup"><span data-stu-id="278e2-101">Create MailFolder</span></span>

<span data-ttu-id="278e2-102">Use esta API para crear un objeto mailfolder secundario.</span><span class="sxs-lookup"><span data-stu-id="278e2-102">Use this API to create a new child mailfolder.</span></span>

## <a name="permissions"></a><span data-ttu-id="278e2-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="278e2-103">Permissions</span></span>

<span data-ttu-id="278e2-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="278e2-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="278e2-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="278e2-106">Permission type</span></span> | <span data-ttu-id="278e2-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="278e2-107">Permissions (from least to most privileged)</span></span> |
|:----------------|:--------------------------------------------|
|<span data-ttu-id="278e2-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="278e2-108">Delegated (work or school account)</span></span> | <span data-ttu-id="278e2-109">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="278e2-109">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="278e2-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="278e2-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="278e2-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="278e2-111">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="278e2-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="278e2-112">Application</span></span> | <span data-ttu-id="278e2-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="278e2-113">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="278e2-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="278e2-114">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /me/mailFolders/{id}/childFolders
POST /users/{id | userPrincipalName}/mailFolders/{id}/childFolders
```

<span data-ttu-id="278e2-115">Especifique la carpeta principal en la dirección URL de consulta como identificador de la carpeta o el nombre de carpeta conocido.</span><span class="sxs-lookup"><span data-stu-id="278e2-115">Specify the parent folder in the query URL as a folder ID, or the , , , or  well-known folder name.</span></span> <span data-ttu-id="278e2-116">Para obtener una lista de los nombres de carpetas conocidos compatibles, vea [Tipo de recurso mailFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="278e2-116">For a list of supported well-known folder names, see [mailFolder resource type](../resources/mailfolder.md).</span></span>

## <a name="request-headers"></a><span data-ttu-id="278e2-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="278e2-117">Request headers</span></span>

| <span data-ttu-id="278e2-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="278e2-118">Header</span></span> | <span data-ttu-id="278e2-119">Valor</span><span class="sxs-lookup"><span data-stu-id="278e2-119">Value</span></span> |
|:-------|:------|
| <span data-ttu-id="278e2-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="278e2-120">Authorization</span></span> | <span data-ttu-id="278e2-121">`Bearer {token}`.</span><span class="sxs-lookup"><span data-stu-id="278e2-121"></span></span> <span data-ttu-id="278e2-122">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="278e2-122">Required.</span></span> |
| <span data-ttu-id="278e2-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="278e2-123">Content-Type</span></span> | <span data-ttu-id="278e2-124">`application/json`.</span><span class="sxs-lookup"><span data-stu-id="278e2-124"></span></span> <span data-ttu-id="278e2-125">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="278e2-125">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="278e2-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="278e2-126">Request body</span></span>

<span data-ttu-id="278e2-127">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="278e2-127">In the request body, provide a JSON object with the following parameters.</span></span> <span data-ttu-id="278e2-128">**displayName** es la única propiedad grabable de un objeto [mailFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="278e2-128">**displayName** is the only writable property for a [mailFolder](../resources/mailfolder.md) object.</span></span>

| <span data-ttu-id="278e2-129">Parámetro</span><span class="sxs-lookup"><span data-stu-id="278e2-129">Parameter</span></span> | <span data-ttu-id="278e2-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="278e2-130">Type</span></span> | <span data-ttu-id="278e2-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="278e2-131">Description</span></span> |
|:----------|:-----|:------------|
|<span data-ttu-id="278e2-132">displayName</span><span class="sxs-lookup"><span data-stu-id="278e2-132">displayName</span></span>|<span data-ttu-id="278e2-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="278e2-133">String</span></span>|<span data-ttu-id="278e2-134">Nombre para mostrar de la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="278e2-134">The display name of the new folder.</span></span>|

## <a name="response"></a><span data-ttu-id="278e2-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="278e2-135">Response</span></span>

<span data-ttu-id="278e2-136">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y un recurso [mailFolder](../resources/mailfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="278e2-136">If successful, this method returns a `201 Created` response code and [mailFolder](../resources/mailfolder.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="278e2-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="278e2-137">Example</span></span>

##### <a name="request"></a><span data-ttu-id="278e2-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="278e2-138">Request</span></span>

<span data-ttu-id="278e2-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="278e2-139">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="278e2-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="278e2-140">Response</span></span>
<span data-ttu-id="278e2-141">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="278e2-141">Here is an example of the response.</span></span>

> <span data-ttu-id="278e2-p106">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="278e2-p106">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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
