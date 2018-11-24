# <a name="list-the-published-apps-from-the-microsoft-teams-app-catalog"></a><span data-ttu-id="3c70a-101">Lista de las aplicaciones publicadas desde el catálogo de aplicaciones de Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="3c70a-101">List the published apps from the Microsoft Teams app catalog</span></span>



<span data-ttu-id="3c70a-102">Lista de [aplicaciones](../resources/teamsapp.md) desde el catálogo de aplicaciones de Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="3c70a-102">List [apps](../resources/teamsapp.md) from the Microsoft Teams app catalog.</span></span> <span data-ttu-id="3c70a-103">Esto incluye aplicaciones de la tienda de Microsoft Teams, así como aplicaciones de catálogo de aplicaciones de la organización (el catálogo de aplicaciones de inquilino).</span><span class="sxs-lookup"><span data-stu-id="3c70a-103">This includes apps from the Microsoft Teams store, as well as apps from your organization's app catalog (the tenant app catalog).</span></span> <span data-ttu-id="3c70a-104">Para obtener aplicaciones desde el catálogo de aplicaciones de la organización sólo, especifique `Organization` como el **distributionMethod** en el recurso [teamsCatalogApp](../resources/teamsapp.md) .</span><span class="sxs-lookup"><span data-stu-id="3c70a-104">To get apps from your organization's app catalog only, specify `Organization` as the **distributionMethod** in the [teamsCatalogApp](../resources/teamsapp.md) resource.</span></span>

## <a name="permissions"></a><span data-ttu-id="3c70a-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="3c70a-105">Permissions</span></span>

<span data-ttu-id="3c70a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](https://developer.microsoft.com/graph/docs/concepts/permissions_reference).</span><span class="sxs-lookup"><span data-stu-id="3c70a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](https://developer.microsoft.com/graph/docs/concepts/permissions_reference).</span></span>

><span data-ttu-id="3c70a-108">**Nota:** Sólo los administradores globales pueden llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="3c70a-108">**Note:** Only global administrators can call this API.</span></span> 

| <span data-ttu-id="3c70a-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3c70a-109">Permission Type</span></span>                        | <span data-ttu-id="3c70a-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3c70a-110">Permissions (from least to most privileged)</span></span>|
|:----------------------------------     |:-------------|
| <span data-ttu-id="3c70a-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3c70a-111">Delegated (work or school account)</span></span>     | <span data-ttu-id="3c70a-112">AppCatalog.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3c70a-112">AppCatalog.ReadWrite.All</span></span> |
| <span data-ttu-id="3c70a-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3c70a-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3c70a-114">No admitido</span><span class="sxs-lookup"><span data-stu-id="3c70a-114">Not supported</span></span>|
| <span data-ttu-id="3c70a-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3c70a-115">Application</span></span>                            | <span data-ttu-id="3c70a-116">No se admite</span><span class="sxs-lookup"><span data-stu-id="3c70a-116">Not supported</span></span>|

## <a name="http-request"></a><span data-ttu-id="3c70a-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3c70a-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /appCatalogs/teamsApps
```

## <a name="optional-query-parameters"></a><span data-ttu-id="3c70a-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="3c70a-118">Optional query parameters</span></span>
<span data-ttu-id="3c70a-119">Este método admite la $filter, $select, y $expanda [parámetros de consulta de OData](../../../concepts/query_parameters.md) para ayudar a personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3c70a-119">This method supports the $filter, $select, and $expand [OData query parameters](../../../concepts/query_parameters.md) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="3c70a-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3c70a-120">Request headers</span></span>

| <span data-ttu-id="3c70a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3c70a-121">Header</span></span>        | <span data-ttu-id="3c70a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="3c70a-122">Value</span></span>           |
|:--------------|:--------------  |
| <span data-ttu-id="3c70a-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="3c70a-123">Authorization</span></span> | <span data-ttu-id="3c70a-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3c70a-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="3c70a-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3c70a-126">Request body</span></span>
<span data-ttu-id="3c70a-127">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="3c70a-127">None.</span></span>

><span data-ttu-id="3c70a-128">**Nota:** Puede filtrar en cualquiera de los campos del objeto [teamsCatalogApp](../resources/teamsapp.md) para reducir la lista de resultados.</span><span class="sxs-lookup"><span data-stu-id="3c70a-128">**Note:** You can filter on any of the fields of the [teamsCatalogApp](../resources/teamsapp.md) object to shorten the list of results.</span></span> <span data-ttu-id="3c70a-129">Puede usar cualquiera de las siguientes operaciones de filtro: igual, no igual y, o bien y no.</span><span class="sxs-lookup"><span data-stu-id="3c70a-129">You can use any of the following filter operations: Equal, not-equal, and, or, and not.</span></span>

## <a name="response"></a><span data-ttu-id="3c70a-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3c70a-130">Response</span></span>
<span data-ttu-id="3c70a-131">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una lista de objetos de [teamsCatalogApp](../resources/teamsapp.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3c70a-131">If successful, this method returns a `200 OK` response code and a list of [teamsCatalogApp](../resources/teamsapp.md) objects in the response body.</span></span>

## <a name="examples"></a><span data-ttu-id="3c70a-132">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3c70a-132">Examples</span></span>
### <a name="example-1"></a><span data-ttu-id="3c70a-133">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="3c70a-133">Example 1</span></span>
<span data-ttu-id="3c70a-134">En el ejemplo siguiente se enumeran todas las aplicaciones que son específicas de su inquilino.</span><span class="sxs-lookup"><span data-stu-id="3c70a-134">The following example lists all applications that are specific to your tenant.</span></span>

#### <a name="request"></a><span data-ttu-id="3c70a-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3c70a-135">Request</span></span>
```
GET https://graph.microsoft.com/beta/appCatalogs/teamsApps?$filter=distributionMethod eq 'organization'
```

#### <a name="response"></a><span data-ttu-id="3c70a-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3c70a-136">Response</span></span>
```
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "id": "b1c5353a-7aca-41b3-830f-27d5218fe0e5",
      "externalId": "f31b1263-ba99-435a-a679-911d24850d7c",
      "name": "Test App",
      "version": "1.0.1",
      "distributionMethod":"Organization"
    }
  ]
}
```

### <a name="example-2"></a><span data-ttu-id="3c70a-137">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="3c70a-137">Example 2</span></span>

<span data-ttu-id="3c70a-138">En el ejemplo siguiente se enumeran las aplicaciones con un identificador determinado.</span><span class="sxs-lookup"><span data-stu-id="3c70a-138">The following example lists applications with a given ID.</span></span>

#### <a name="request"></a><span data-ttu-id="3c70a-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3c70a-139">Request</span></span>
```
GET https://graph.microsoft.com/beta/appCatalogs/teamsApps?$filter=id%20eq%20'b1c5353a-7aca-41b3-830f-27d5218fe0e5'
```

#### <a name="response"></a><span data-ttu-id="3c70a-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3c70a-140">Response</span></span>
```
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "id": "b1c5353a-7aca-41b3-830f-27d5218fe0e5",
      "externalId": "f31b1263-ba99-435a-a679-911d24850d7c",
      "name": "Test App",
      "version": "1.0.1",
      "distributionMethod":"Organization"
    }
  ]
}
```

