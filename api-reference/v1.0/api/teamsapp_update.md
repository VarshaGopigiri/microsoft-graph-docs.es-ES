# <a name="update-apps-published-to-your-organizations-app-catalog"></a><span data-ttu-id="65183-101">Actualizar aplicaciones publicadas en catálogo de aplicaciones de la organización</span><span class="sxs-lookup"><span data-stu-id="65183-101">Update apps published to your organization's app catalog</span></span>



<span data-ttu-id="65183-102">Actualización de una [aplicación](../resources/teamsapp.md) se publicaron anteriormente en el catálogo de aplicaciones de Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="65183-102">Update an [app](../resources/teamsapp.md) previously published to the Microsoft Teams app catalog.</span></span> <span data-ttu-id="65183-103">Esta API específicamente actualiza una aplicación publicada en catálogo de aplicaciones de la organización (el catálogo de aplicaciones de inquilino).</span><span class="sxs-lookup"><span data-stu-id="65183-103">This API specifically updates an app published to your organization's app catalog (the tenant app catalog).</span></span> <span data-ttu-id="65183-104">Para publicar en el catálogo de aplicaciones de la organización, especifique `organization` como el **distributionMethod** en el recurso [teamsCatalogApp](../resources/teamsapp.md) .</span><span class="sxs-lookup"><span data-stu-id="65183-104">To publish to your organization's app catalog, specify `organization` as the **distributionMethod** in the [teamsCatalogApp](../resources/teamsapp.md) resource.</span></span>

## <a name="permissions"></a><span data-ttu-id="65183-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="65183-105">Permissions</span></span>

<span data-ttu-id="65183-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](https://developer.microsoft.com/graph/docs/concepts/permissions_reference).</span><span class="sxs-lookup"><span data-stu-id="65183-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](https://developer.microsoft.com/graph/docs/concepts/permissions_reference).</span></span>

><span data-ttu-id="65183-108">**Nota:** Sólo los administradores globales pueden llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="65183-108">**Note:** Only global administrators can call this API.</span></span>

| <span data-ttu-id="65183-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="65183-109">Permission Type</span></span>                        | <span data-ttu-id="65183-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="65183-110">Permissions (from least to most privileged)</span></span>|
|:----------------------------------     |:-------------|
| <span data-ttu-id="65183-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="65183-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="65183-112">AppCatalog.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="65183-112">AppCatalog.ReadWrite.All</span></span> |
| <span data-ttu-id="65183-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="65183-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="65183-114">No admitido</span><span class="sxs-lookup"><span data-stu-id="65183-114">Not supported</span></span>|
| <span data-ttu-id="65183-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="65183-115">Application</span></span>                            | <span data-ttu-id="65183-116">No se admite</span><span class="sxs-lookup"><span data-stu-id="65183-116">Not supported</span></span>|

## <a name="http-request"></a><span data-ttu-id="65183-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="65183-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PUT /appCatalogs/teamsApps/{id}
```

## <a name="request-headers"></a><span data-ttu-id="65183-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="65183-118">Request headers</span></span>

| <span data-ttu-id="65183-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="65183-119">Header</span></span>        | <span data-ttu-id="65183-120">Valor</span><span class="sxs-lookup"><span data-stu-id="65183-120">Value</span></span>           |
|:--------------|:--------------  |
| <span data-ttu-id="65183-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="65183-121">Authorization</span></span> | <span data-ttu-id="65183-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="65183-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="65183-124">Content-Type</span><span class="sxs-lookup"><span data-stu-id="65183-124">Content-Type</span></span>  | <span data-ttu-id="65183-125">aplicación/zip</span><span class="sxs-lookup"><span data-stu-id="65183-125">application/zip</span></span> |

## <a name="request-body"></a><span data-ttu-id="65183-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="65183-126">Request body</span></span>

<span data-ttu-id="65183-127">Carga de los equipos Zip manifiesto: Para la aplicación de los equipos zip archivo [consulte Creación de un paquete de aplicación](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package)</span><span class="sxs-lookup"><span data-stu-id="65183-127">Teams Zip Manifest Payload: For Teams application zip file [see Create an app package](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package)</span></span>

><span data-ttu-id="65183-128">**Nota:** Use el identificador devuelto de la llamada [lista publica aplicaciones](./teamsapp_list.md) para hacer referencia a la aplicación que desea actualizar.</span><span class="sxs-lookup"><span data-stu-id="65183-128">**Note:** Use the ID returned from the [List published apps](./teamsapp_list.md) call for to reference the app you'd like to update.</span></span> <span data-ttu-id="65183-129">No use el identificador del manifiesto del paquete de la aplicación de zip.</span><span class="sxs-lookup"><span data-stu-id="65183-129">Do not use the ID from the manifest of the zip app package.</span></span>

## <a name="response"></a><span data-ttu-id="65183-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="65183-130">Response</span></span>

```
HTTP/1.1 204 No Content
```

## <a name="example"></a><span data-ttu-id="65183-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="65183-131">Example</span></span>

### <a name="request"></a><span data-ttu-id="65183-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="65183-132">Request</span></span>

```
PUT https://graph.microsoft.com/beta/appCatalogs/teamsApps/06805b9e-77e3-4b93-ac81-525eb87513b8
Content-type: application/zip
Content-length: 244

[Zip file containing a Teams app package]
```

<span data-ttu-id="65183-133">Para la aplicación de los equipos zip archivo [vea Crear paquete de la aplicación](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package)</span><span class="sxs-lookup"><span data-stu-id="65183-133">For Teams application zip file [see Create app package](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package)</span></span>

### <a name="response"></a><span data-ttu-id="65183-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="65183-134">Response</span></span>

```
HTTP/1.1 204 No Content
```
