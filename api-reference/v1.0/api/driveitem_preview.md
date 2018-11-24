# <a name="driveitem-preview"></a><span data-ttu-id="d3efe-101">driveItem: vista previa</span><span class="sxs-lookup"><span data-stu-id="d3efe-101">driveItem: preview</span></span>

<span data-ttu-id="d3efe-102">Esta acción le permite obtener corta duración puede incrustar las direcciones URL de un elemento con el fin de representar una vista previa temporal.</span><span class="sxs-lookup"><span data-stu-id="d3efe-102">This action allows you to obtain short-lived embeddable URLs for an item in order to render a temporary preview.</span></span>

<span data-ttu-id="d3efe-103">Si desea obtener vínculos puede incrustar larga duración, use la API [createLink][] en su lugar.</span><span class="sxs-lookup"><span data-stu-id="d3efe-103">If you want to obtain long-lived embeddable links, use the [createLink][] API instead.</span></span>

> <span data-ttu-id="d3efe-104">**Nota:** Actualmente, la acción de **vista previa** sólo está disponible en SharePoint y OneDrive para la empresa.</span><span class="sxs-lookup"><span data-stu-id="d3efe-104">**Note:** The **preview** action is currently only available on SharePoint and OneDrive for Business.</span></span>

[createLink]: driveItem_createLink.md

## <a name="permissions"></a><span data-ttu-id="d3efe-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="d3efe-106">Permissions</span></span>

<span data-ttu-id="d3efe-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="d3efe-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="d3efe-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d3efe-109">Permission type</span></span>                        | <span data-ttu-id="d3efe-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d3efe-110">Permissions (from least to most privileged)</span></span>
|:---------------------------------------|:-------------------------------------------
| <span data-ttu-id="d3efe-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d3efe-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="d3efe-112">Files.Read, Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d3efe-112">Files.Read, Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>
| <span data-ttu-id="d3efe-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d3efe-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d3efe-114">Files.Read, Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d3efe-114">Files.Read, Files.ReadWrite, Files.ReadWrite.All</span></span>
| <span data-ttu-id="d3efe-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d3efe-115">Application</span></span>                            | <span data-ttu-id="d3efe-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d3efe-116">Not supported.</span></span>

## <a name="http-request"></a><span data-ttu-id="d3efe-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d3efe-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /drives/{driveId}/items/{itemId}/preview
POST /groups/{groupId}/drive/items/{itemId}/preview
POST /me/drive/items/{itemId}/preview
POST /sites/{siteId}/drive/items/{itemId}/preview
POST /users/{userId}/drive/items/{itemId}/preview
POST /shares/{shareId}/driveItem/preview
```

## <a name="request-body"></a><span data-ttu-id="d3efe-118">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d3efe-118">Request body</span></span>

<span data-ttu-id="d3efe-119">El cuerpo de la solicitud define las propiedades de la dirección URL puede incrustar está solicitando la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d3efe-119">The body of the request defines properties of the embeddable URL your application is requesting.</span></span>
<span data-ttu-id="d3efe-120">La solicitud debe ser un objeto JSON con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="d3efe-120">The request should be a JSON object with the following properties.</span></span>

|   <span data-ttu-id="d3efe-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="d3efe-121">Name</span></span>      |  <span data-ttu-id="d3efe-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="d3efe-122">Type</span></span>         | <span data-ttu-id="d3efe-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3efe-123">Description</span></span>
|:------------|:--------------|:-----------------------------------------------
| <span data-ttu-id="d3efe-124">page</span><span class="sxs-lookup"><span data-stu-id="d3efe-124">page</span></span>        | <span data-ttu-id="d3efe-125">cadena o número</span><span class="sxs-lookup"><span data-stu-id="d3efe-125">string/number</span></span> | <span data-ttu-id="d3efe-126">Opcional.</span><span class="sxs-lookup"><span data-stu-id="d3efe-126">Optional.</span></span> <span data-ttu-id="d3efe-127">Número de página del documento para iniciar en, si procede.</span><span class="sxs-lookup"><span data-stu-id="d3efe-127">Page number of document to start at, if applicable.</span></span> <span data-ttu-id="d3efe-128">Especificado como cadena para los casos de uso futuro alrededor de tipos de archivo como ZIP.</span><span class="sxs-lookup"><span data-stu-id="d3efe-128">Specified as string for future use cases around file types such as ZIP.</span></span>
| <span data-ttu-id="d3efe-129">zoom</span><span class="sxs-lookup"><span data-stu-id="d3efe-129">zoom</span></span>        | <span data-ttu-id="d3efe-130">n?mero</span><span class="sxs-lookup"><span data-stu-id="d3efe-130">number</span></span>        | <span data-ttu-id="d3efe-131">Opcional.</span><span class="sxs-lookup"><span data-stu-id="d3efe-131">Optional.</span></span> <span data-ttu-id="d3efe-132">Aumentar nivel para iniciar en, si procede.</span><span class="sxs-lookup"><span data-stu-id="d3efe-132">Zoom level to start at, if applicable.</span></span>

## <a name="response"></a><span data-ttu-id="d3efe-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d3efe-133">Response</span></span>

```json
{
    "getUrl": "https://www.onedrive.com/embed?foo=bar&bar=baz",
    "postParameters": "param1=value&param2=another%20value",
    "postUrl": "https://www.onedrive.com/embed_by_post"
}
```

<span data-ttu-id="d3efe-134">La respuesta será un objeto JSON que contiene las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="d3efe-134">The response will be a JSON object containing the following properties:</span></span>

| <span data-ttu-id="d3efe-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="d3efe-135">Name</span></span>           | <span data-ttu-id="d3efe-136">Tipo</span><span class="sxs-lookup"><span data-stu-id="d3efe-136">Type</span></span>   | <span data-ttu-id="d3efe-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3efe-137">Description</span></span>
|:---------------|:-------|:---------------------------------------------------
| <span data-ttu-id="d3efe-138">getUrl</span><span class="sxs-lookup"><span data-stu-id="d3efe-138">getUrl</span></span>         | <span data-ttu-id="d3efe-139">string</span><span class="sxs-lookup"><span data-stu-id="d3efe-139">string</span></span> | <span data-ttu-id="d3efe-140">Dirección URL adecuada para incrustar mediante HTTP GET (IFRAME, etcetera).</span><span class="sxs-lookup"><span data-stu-id="d3efe-140">URL suitable for embedding using HTTP GET (iframes, etc.)</span></span>
| <span data-ttu-id="d3efe-141">URL para exponer</span><span class="sxs-lookup"><span data-stu-id="d3efe-141">postUrl</span></span>        | <span data-ttu-id="d3efe-142">string</span><span class="sxs-lookup"><span data-stu-id="d3efe-142">string</span></span> | <span data-ttu-id="d3efe-143">Dirección URL adecuada para incrustar el uso de HTTP POST (de envío de formulario, JS, etcetera.)</span><span class="sxs-lookup"><span data-stu-id="d3efe-143">URL suitable for embedding using HTTP POST (form post, JS, etc.)</span></span>
| <span data-ttu-id="d3efe-144">postParameters</span><span class="sxs-lookup"><span data-stu-id="d3efe-144">postParameters</span></span> | <span data-ttu-id="d3efe-145">string</span><span class="sxs-lookup"><span data-stu-id="d3efe-145">string</span></span> | <span data-ttu-id="d3efe-146">Parámetros de entrada para incluir si usa URL para exponer</span><span class="sxs-lookup"><span data-stu-id="d3efe-146">POST parameters to include if using postUrl</span></span>

<span data-ttu-id="d3efe-147">Es posible que se devolverá getUrl, URL para exponer o ambos según el estado actual del embed compatibilidad con las opciones especificadas.</span><span class="sxs-lookup"><span data-stu-id="d3efe-147">Either getUrl, postUrl, or both might be returned depending on the current state of embed support for the specified options.</span></span>

<span data-ttu-id="d3efe-148">postParameters es una cadena con formato como `application/x-www-form-urlencoded`, y si se realiza una entrada a la URL para exponer el tipo de contenido se debe establecer en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="d3efe-148">postParameters is a string formatted as `application/x-www-form-urlencoded`, and if performing a POST to the postUrl the content-type should be set accordingly.</span></span> <span data-ttu-id="d3efe-149">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="d3efe-149">For example:</span></span>
```
POST https://www.onedrive.com/embed_by_post
Content-Type: application/x-www-form-urlencoded

param1=value&param2=another%20value
```

### <a name="pagezoom"></a><span data-ttu-id="d3efe-150">Página/zoom</span><span class="sxs-lookup"><span data-stu-id="d3efe-150">Page/zoom</span></span>

<span data-ttu-id="d3efe-151">Las opciones de 'zoom' y 'page' podrían no estar disponibles para todas las aplicaciones de vista previa, pero se aplicará si lo admite la aplicación de vista previa.</span><span class="sxs-lookup"><span data-stu-id="d3efe-151">The 'page' and 'zoom' options may not be available for all preview apps, but will be applied if the preview app supports it.</span></span>
