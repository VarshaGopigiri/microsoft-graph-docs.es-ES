# <a name="remove-an-app-from-your-organizations-app-catalog"></a><span data-ttu-id="b639c-101">Quitar una aplicación de catálogo de aplicaciones de la organización</span><span class="sxs-lookup"><span data-stu-id="b639c-101">Remove an app from your organization's app catalog</span></span>



<span data-ttu-id="b639c-102">Quitar la [aplicación](../resources/teamsapp.md) de catálogo de aplicaciones de la organización (el catálogo de aplicaciones de inquilino).</span><span class="sxs-lookup"><span data-stu-id="b639c-102">Remove the [app](../resources/teamsapp.md) from your organization's app catalog (the tenant app catalog).</span></span> <span data-ttu-id="b639c-103">Para quitar la aplicación de catálogo de aplicaciones de la organización, especifique `organization` como el **distributionMethod** en el recurso [teamsCatalogApp](../resources/teamsapp.md) .</span><span class="sxs-lookup"><span data-stu-id="b639c-103">To remove your app from your organization's app catalog, specify `organization` as the **distributionMethod** in the [teamsCatalogApp](../resources/teamsapp.md) resource.</span></span>

## <a name="permissions"></a><span data-ttu-id="b639c-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="b639c-104">Permissions</span></span>

<span data-ttu-id="b639c-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](https://developer.microsoft.com/graph/docs/concepts/permissions_reference).</span><span class="sxs-lookup"><span data-stu-id="b639c-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](https://developer.microsoft.com/graph/docs/concepts/permissions_reference).</span></span>

><span data-ttu-id="b639c-107">**Nota:** Sólo los administradores globales pueden llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="b639c-107">**Note:** Only global administrators can call this API.</span></span> 

| <span data-ttu-id="b639c-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b639c-108">Permission Type</span></span>                        | <span data-ttu-id="b639c-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b639c-109">Permissions (from least to most privileged)</span></span>|
|:----------------------------------     |:-------------|
| <span data-ttu-id="b639c-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b639c-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="b639c-111">AppCatalog.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b639c-111">AppCatalog.ReadWrite.All</span></span> |
| <span data-ttu-id="b639c-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b639c-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b639c-113">No admitido</span><span class="sxs-lookup"><span data-stu-id="b639c-113">Not supported</span></span>|
| <span data-ttu-id="b639c-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b639c-114">Application</span></span>                            | <span data-ttu-id="b639c-115">No se admite</span><span class="sxs-lookup"><span data-stu-id="b639c-115">Not supported</span></span>|

## <a name="http-request"></a><span data-ttu-id="b639c-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b639c-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /appCatalogs/teamsApps/{id}
```

## <a name="request-headers"></a><span data-ttu-id="b639c-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b639c-117">Request headers</span></span>

| <span data-ttu-id="b639c-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b639c-118">Header</span></span>        | <span data-ttu-id="b639c-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b639c-119">Value</span></span>           |
|:--------------|:--------------  |
| <span data-ttu-id="b639c-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="b639c-120">Authorization</span></span> | <span data-ttu-id="b639c-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b639c-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="b639c-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b639c-123">Request body</span></span>

<span data-ttu-id="b639c-124">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b639c-124">None.</span></span>

><span data-ttu-id="b639c-125">**Nota:** Use el identificador devuelto de la llamada [lista publica aplicaciones](./teamsapp_list.md) para hacer referencia a la aplicación que desea actualizar.</span><span class="sxs-lookup"><span data-stu-id="b639c-125">**Note:** Use the ID returned from the [List published apps](./teamsapp_list.md) call for to reference the app you'd like to update.</span></span> <span data-ttu-id="b639c-126">No use el identificador del manifiesto del paquete de la aplicación de zip.</span><span class="sxs-lookup"><span data-stu-id="b639c-126">Do not use the ID from the manifest of the zip app package.</span></span>

## <a name="response"></a><span data-ttu-id="b639c-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b639c-127">Response</span></span>

```
HTTP/1.1 204 No Content
```

## <a name="example"></a><span data-ttu-id="b639c-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b639c-128">Example</span></span>

### <a name="request"></a><span data-ttu-id="b639c-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b639c-129">Request</span></span>

```http
DELETE https://graph.microsoft.com/beta/appCatalogs/teamsApps/06805b9e-77e3-4b93-ac81-525eb87513b8
```

### <a name="response"></a><span data-ttu-id="b639c-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b639c-130">Response</span></span>

```http
HTTP/1.1 204 No Content
```
