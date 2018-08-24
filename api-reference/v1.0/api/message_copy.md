# <a name="message-copy"></a><span data-ttu-id="d7760-101">message: copy</span><span class="sxs-lookup"><span data-stu-id="d7760-101">message: copy</span></span>

<span data-ttu-id="d7760-102">Copia un mensaje a una carpeta.</span><span class="sxs-lookup"><span data-stu-id="d7760-102">Copy a message to a folder.</span></span>

## <a name="permissions"></a><span data-ttu-id="d7760-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="d7760-103">Permissions</span></span>

<span data-ttu-id="d7760-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="d7760-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="d7760-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d7760-106">Permission type</span></span> | <span data-ttu-id="d7760-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d7760-107">Permissions (from least to most privileged)</span></span> |
|:----------------|:--------------------------------------------|
|<span data-ttu-id="d7760-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d7760-108">Delegated (work or school account)</span></span> | <span data-ttu-id="d7760-109">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d7760-109">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="d7760-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d7760-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d7760-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d7760-111">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="d7760-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d7760-112">Application</span></span> | <span data-ttu-id="d7760-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d7760-113">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="d7760-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d7760-114">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /me/messages/{id}/copy
POST /users/{id | userPrincipalName}/messages/{id}/copy
POST /me/mailFolders/{id}/messages/{id}/copy
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/copy
```

## <a name="request-headers"></a><span data-ttu-id="d7760-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d7760-115">Request headers</span></span>

| <span data-ttu-id="d7760-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7760-116">Header</span></span> | <span data-ttu-id="d7760-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d7760-117">Value</span></span> |
|:-------|:------|
| <span data-ttu-id="d7760-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="d7760-118">Authorization</span></span> | <span data-ttu-id="d7760-119">`Bearer {token}`.</span><span class="sxs-lookup"><span data-stu-id="d7760-119"></span></span> <span data-ttu-id="d7760-120">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d7760-120">Required.</span></span> |
| <span data-ttu-id="d7760-121">Content-Type</span><span class="sxs-lookup"><span data-stu-id="d7760-121">Content-Type</span></span> | <span data-ttu-id="d7760-122">`application/json`.</span><span class="sxs-lookup"><span data-stu-id="d7760-122"></span></span> <span data-ttu-id="d7760-123">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d7760-123">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="d7760-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d7760-124">Request body</span></span>

<span data-ttu-id="d7760-125">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="d7760-125">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="d7760-126">Parámetro</span><span class="sxs-lookup"><span data-stu-id="d7760-126">Parameter</span></span> | <span data-ttu-id="d7760-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="d7760-127">Type</span></span> | <span data-ttu-id="d7760-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7760-128">Description</span></span> |
|:----------|:-----|:------------|
|<span data-ttu-id="d7760-129">destinationId</span><span class="sxs-lookup"><span data-stu-id="d7760-129">destinationId</span></span>|<span data-ttu-id="d7760-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="d7760-130">String</span></span>|<span data-ttu-id="d7760-131">El identificador de la carpeta de destino, o un nombre de carpeta conocido.</span><span class="sxs-lookup"><span data-stu-id="d7760-131">The destination folder ID, or the , , , or  well-known folder name.</span></span> <span data-ttu-id="d7760-132">Para obtener una lista de los nombres de carpetas conocidos compatibles, vea [Tipo de recurso mailFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="d7760-132">For a list of supported well-known folder names, see [mailFolder resource type](../resources/mailfolder.md).</span></span>|

## <a name="response"></a><span data-ttu-id="d7760-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d7760-133">Response</span></span>

<span data-ttu-id="d7760-134">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y un recurso [message](../resources/message.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d7760-134">If successful, this method returns a `201 Created` response code and a [sharedDriveItem](../resources/message.md) resource in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d7760-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d7760-135">Example</span></span>

<span data-ttu-id="d7760-136">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="d7760-136">Here is an example of how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="d7760-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d7760-137">Request</span></span>
<span data-ttu-id="d7760-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d7760-138">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "message_copy"
}-->

```http
POST https://graph.microsoft.com/v1.0/me/messages/{id}/copy
Content-type: application/json
Content-length: 44

{
  "destinationId": "destinationId-value"
}
```

##### <a name="response"></a><span data-ttu-id="d7760-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d7760-139">Response</span></span>

<span data-ttu-id="d7760-140">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d7760-140">Here is an example of the response.</span></span>

> <span data-ttu-id="d7760-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d7760-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 248

{
  "receivedDateTime": "datetime-value",
  "sentDateTime": "datetime-value",
  "hasAttachments": true,
  "subject": "subject-value",
  "body": {
    "contentType": "",
    "content": "content-value"
  },
  "bodyPreview": "bodyPreview-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "message: copy",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
