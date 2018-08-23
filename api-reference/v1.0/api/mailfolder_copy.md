# <a name="mailfolder-copy"></a><span data-ttu-id="3473d-101">mailFolder: copy</span><span class="sxs-lookup"><span data-stu-id="3473d-101">mailFolder: copy</span></span>

<span data-ttu-id="3473d-102">Copia un objeto mailfolder y su contenido en otro objeto mailfolder.</span><span class="sxs-lookup"><span data-stu-id="3473d-102">Copy a mailfolder and its contents to another mailfolder.</span></span>

## <a name="permissions"></a><span data-ttu-id="3473d-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="3473d-103">Permissions</span></span>

<span data-ttu-id="3473d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="3473d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="3473d-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3473d-106">Permission type</span></span> | <span data-ttu-id="3473d-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3473d-107">Permissions (from least to most privileged)</span></span> |
|:----------------|:--------------------------------------------|
|<span data-ttu-id="3473d-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3473d-108">Delegated (work or school account)</span></span> | <span data-ttu-id="3473d-109">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3473d-109">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="3473d-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3473d-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3473d-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3473d-111">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="3473d-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3473d-112">Application</span></span> | <span data-ttu-id="3473d-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3473d-113">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="3473d-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3473d-114">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /me/mailFolders/{id}/copy
POST /users/{id | userPrincipalName}/mailFolders/{id}/copy
```

## <a name="request-headers"></a><span data-ttu-id="3473d-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3473d-115">Request headers</span></span>
| <span data-ttu-id="3473d-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3473d-116">Header</span></span> | <span data-ttu-id="3473d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="3473d-117">Value</span></span> |
|:-------|:------|
| <span data-ttu-id="3473d-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="3473d-118">Authorization</span></span> | <span data-ttu-id="3473d-119">`Bearer {token}`.</span><span class="sxs-lookup"><span data-stu-id="3473d-119"></span></span> <span data-ttu-id="3473d-120">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3473d-120">Required.</span></span> |
| <span data-ttu-id="3473d-121">Content-Type</span><span class="sxs-lookup"><span data-stu-id="3473d-121">Content-Type</span></span> | <span data-ttu-id="3473d-122">`application/json`.</span><span class="sxs-lookup"><span data-stu-id="3473d-122"></span></span> <span data-ttu-id="3473d-123">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3473d-123">Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="3473d-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3473d-124">Request body</span></span>

<span data-ttu-id="3473d-125">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="3473d-125">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="3473d-126">Parámetro</span><span class="sxs-lookup"><span data-stu-id="3473d-126">Parameter</span></span> | <span data-ttu-id="3473d-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="3473d-127">Type</span></span> | <span data-ttu-id="3473d-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="3473d-128">Description</span></span> |
|:----------|:-----|:------------|
|<span data-ttu-id="3473d-129">destinationId</span><span class="sxs-lookup"><span data-stu-id="3473d-129">destinationId</span></span>|<span data-ttu-id="3473d-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="3473d-130">String</span></span>|<span data-ttu-id="3473d-131">El identificador de la carpeta, o un nombre de carpeta conocido.</span><span class="sxs-lookup"><span data-stu-id="3473d-131">The destination folder ID, or the , , , or  well-known folder name.</span></span> <span data-ttu-id="3473d-132">Para obtener una lista de los nombres de carpetas conocidos compatibles, vea [Tipo de recurso mailFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="3473d-132">For a list of supported well-known folder names, see [mailFolder resource type](../resources/mailfolder.md).</span></span>|

## <a name="response"></a><span data-ttu-id="3473d-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3473d-133">Response</span></span>

<span data-ttu-id="3473d-134">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y un recurso [mailFolder](../resources/mailfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3473d-134">If successful, this method returns a `200 OK` response code and [mailFolder](../resources/mailfolder.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3473d-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3473d-135">Example</span></span>

<span data-ttu-id="3473d-136">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="3473d-136">Here is an example of how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="3473d-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3473d-137">Request</span></span>
<span data-ttu-id="3473d-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3473d-138">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="3473d-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3473d-139">Response</span></span>

<span data-ttu-id="3473d-140">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3473d-140">Here is an example of the response.</span></span>

> <span data-ttu-id="3473d-p105">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3473d-p105">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>
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
