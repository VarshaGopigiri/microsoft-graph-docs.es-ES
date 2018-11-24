# <a name="publish-apps-to-your-organizations-app-catalog"></a><span data-ttu-id="8344e-101">Publicar aplicaciones en el catálogo de aplicaciones de la organización</span><span class="sxs-lookup"><span data-stu-id="8344e-101">Publish apps to your organization's app catalog</span></span>



<span data-ttu-id="8344e-102">Publicar una [aplicación](../resources/teamsapp.md) en el catálogo de aplicaciones de Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="8344e-102">Publish an [app](../resources/teamsapp.md) to the Microsoft Teams apps catalog.</span></span> <span data-ttu-id="8344e-103">En concreto, esta API publica la aplicación al catálogo de su organización (el catálogo de aplicaciones de inquilino); el recurso creado tendrá `distributionMethod`  =  `organization`.</span><span class="sxs-lookup"><span data-stu-id="8344e-103">Specifically, this API publishes the app to your organization's catalog (the tenant app catalog); the created resource will have `distributionMethod` = `organization`.</span></span>

## <a name="permissions"></a><span data-ttu-id="8344e-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="8344e-104">Permissions</span></span>

<span data-ttu-id="8344e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](https://developer.microsoft.com/graph/docs/concepts/permissions_reference).</span><span class="sxs-lookup"><span data-stu-id="8344e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](https://developer.microsoft.com/graph/docs/concepts/permissions_reference).</span></span>

><span data-ttu-id="8344e-107">**Nota:** Sólo los administradores globales pueden llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="8344e-107">**Note:** Only global administrators can call this API.</span></span> 

| <span data-ttu-id="8344e-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8344e-108">Permission Type</span></span>                        | <span data-ttu-id="8344e-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8344e-109">Permissions (from least to most privileged)</span></span>|
|:----------------------------------     |:-------------|
| <span data-ttu-id="8344e-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8344e-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="8344e-111">AppCatalog.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8344e-111">AppCatalog.ReadWrite.All</span></span> |
| <span data-ttu-id="8344e-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8344e-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8344e-113">No admitido</span><span class="sxs-lookup"><span data-stu-id="8344e-113">Not supported</span></span>|
| <span data-ttu-id="8344e-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8344e-114">Application</span></span>                            | <span data-ttu-id="8344e-115">No se admite</span><span class="sxs-lookup"><span data-stu-id="8344e-115">Not supported</span></span>|

## <a name="http-request"></a><span data-ttu-id="8344e-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8344e-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /appCatalogs/teamsApps
```

## <a name="request-headers"></a><span data-ttu-id="8344e-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8344e-117">Request headers</span></span>

| <span data-ttu-id="8344e-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8344e-118">Header</span></span>        | <span data-ttu-id="8344e-119">Valor</span><span class="sxs-lookup"><span data-stu-id="8344e-119">Value</span></span>           |
|:--------------|:--------------  |
| <span data-ttu-id="8344e-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="8344e-120">Authorization</span></span> | <span data-ttu-id="8344e-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8344e-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="8344e-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="8344e-123">Content-Type</span></span>  | <span data-ttu-id="8344e-124">aplicación/zip</span><span class="sxs-lookup"><span data-stu-id="8344e-124">application/zip</span></span> |

## <a name="request-body"></a><span data-ttu-id="8344e-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8344e-125">Request body</span></span>

<span data-ttu-id="8344e-126">Carga de manifiesto Zip de los equipos.</span><span class="sxs-lookup"><span data-stu-id="8344e-126">Teams Zip Manifest Payload.</span></span> <span data-ttu-id="8344e-127">Para la aplicación de los equipos zip de archivo, [vea Crear un paquete de aplicación](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span><span class="sxs-lookup"><span data-stu-id="8344e-127">For Teams application zip file [see Create an app package](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span></span> <span data-ttu-id="8344e-128">No se puede crear una aplicación para una organización que tiene el mismo identificador de manifiesto que otra aplicación en esa organización.</span><span class="sxs-lookup"><span data-stu-id="8344e-128">You can't create an app for an organization that has the same manifest ID as another app in that organization.</span></span>

## <a name="response"></a><span data-ttu-id="8344e-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8344e-129">Response</span></span>

<span data-ttu-id="8344e-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto [teamsCatalogApp](../resources/teamsapp.md) .</span><span class="sxs-lookup"><span data-stu-id="8344e-130">If successful, this method returns a `200 OK` response code and a [teamsCatalogApp](../resources/teamsapp.md) object.</span></span>

## <a name="example"></a><span data-ttu-id="8344e-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8344e-131">Example</span></span>

### <a name="request"></a><span data-ttu-id="8344e-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8344e-132">Request</span></span>

```http
POST https://graph.microsoft.com/beta/appCatalogs/teamsApps
Content-type: application/zip
Content-length: 244

[Zip file containing a Teams app package]
```

<span data-ttu-id="8344e-133">Para obtener información acerca de cómo crear un archivo zip de aplicación de Microsoft Teams, consulte [crear un paquete de aplicación](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span><span class="sxs-lookup"><span data-stu-id="8344e-133">For information about how to create a Microsoft Teams application zip file, see [Create an app package](https://docs.microsoft.com/en-us/microsoftteams/platform/concepts/apps/apps-package).</span></span> 

### <a name="response"></a><span data-ttu-id="8344e-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8344e-134">Response</span></span>

```
HTTP/1.1 201 Created
Content-Type: application/json

{
  "id": "e3e29acb-8c79-412b-b746-e6c39ff4cd22",
  "externalId": "b5561ec9-8cab-4aa3-8aa2-d8d7172e4311",
  "name": "Test App",
  "version": "1.0.0",
  "distributionMethod": "organization"
}
```
