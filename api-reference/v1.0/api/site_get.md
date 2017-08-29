# <a name="get-a-site-resource"></a><span data-ttu-id="3c7a7-101">Obtener un recurso site</span><span class="sxs-lookup"><span data-stu-id="3c7a7-101">Get a site resource</span></span>

<span data-ttu-id="3c7a7-p101">Recupera las propiedades y relaciones de un recurso [site][]. Un recurso **site** representa un sitio de grupo de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="3c7a7-p101">Retrieve properties and relationships for a [site][] resource. A **site** resource represents a team site in SharePoint.</span></span>

<span data-ttu-id="3c7a7-104">[site]: ../resources/site.md</span><span class="sxs-lookup"><span data-stu-id="3c7a7-104">[site]: ../resources/site.md</span></span>

<span data-ttu-id="3c7a7-105">Un recurso **site** se resuelve con un identificador único compuesto de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="3c7a7-105">A **site** is addressed be a unique identifier which is a composite ID of the following values:</span></span>

* <span data-ttu-id="3c7a7-106">Nombre de host de la colección de sitios (contoso.sharepoint.com)</span><span class="sxs-lookup"><span data-stu-id="3c7a7-106">Site collection hostname (contoso.sharepoint.com)</span></span>
* <span data-ttu-id="3c7a7-107">Identificador único (guid) de la colección de sitios</span><span class="sxs-lookup"><span data-stu-id="3c7a7-107">Site collection unique ID (guid)</span></span>
* <span data-ttu-id="3c7a7-108">Identificador único (guid) del sitio</span><span class="sxs-lookup"><span data-stu-id="3c7a7-108">Site unique ID (guid)</span></span>

<span data-ttu-id="3c7a7-109">También hay un identificador de sitio reservado, `root`, que siempre hace referencia al sitio raíz para un destino especificado de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="3c7a7-109">There is also a reserved site identifier, `root`, which always references the root site for a given target, as follows:</span></span>

* <span data-ttu-id="3c7a7-110">`/sites/root`: El sitio raíz del inquilino.</span><span class="sxs-lookup"><span data-stu-id="3c7a7-110">`/sites/root`: The tenant root site.</span></span>
* <span data-ttu-id="3c7a7-111">`/groups/{group-id}/sites/root`: The group's team site.</span><span class="sxs-lookup"><span data-stu-id="3c7a7-111">`/groups/{group-id}/sites/root`: The group's team site.</span></span>

## <a name="permissions"></a><span data-ttu-id="3c7a7-112">Permisos</span><span class="sxs-lookup"><span data-stu-id="3c7a7-112">Permissions</span></span>

<span data-ttu-id="3c7a7-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="3c7a7-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="3c7a7-115">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3c7a7-115">Permission type</span></span>      | <span data-ttu-id="3c7a7-116">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3c7a7-116">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3c7a7-117">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3c7a7-117">Delegated (work or school account)</span></span> | <span data-ttu-id="3c7a7-118">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3c7a7-118">Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="3c7a7-119">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3c7a7-119">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3c7a7-120">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3c7a7-120">Not supported.</span></span>    |
|<span data-ttu-id="3c7a7-121">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3c7a7-121">Application</span></span> | <span data-ttu-id="3c7a7-122">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3c7a7-122">Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="get-the-tenants-root-site"></a><span data-ttu-id="3c7a7-123">Obtener el sitio raíz del inquilino</span><span class="sxs-lookup"><span data-stu-id="3c7a7-123">Get the tenant's root site</span></span>

<span data-ttu-id="3c7a7-124">Para obtener acceso al sitio de SharePoint de raíz dentro de un inquilino:</span><span class="sxs-lookup"><span data-stu-id="3c7a7-124">To access the root SharePoint site within a tenant:</span></span>

```http
GET /sites/root
GET /sites/contoso.sharepoint.com
```

## <a name="access-a-site-by-server-relative-url"></a><span data-ttu-id="3c7a7-125">Obtener acceso a un sitio mediante la dirección URL relativa al servidor</span><span class="sxs-lookup"><span data-stu-id="3c7a7-125">Access a site by server-relative URL</span></span>

<span data-ttu-id="3c7a7-126">Si tiene la dirección URL relativa al servidor de un recurso **site**, puede construir una solicitud de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="3c7a7-126">If you have the server-relative URL for a **site** resource, you can construct a request as follows:</span></span>

```http
GET /sites/{hostname}:/{server-relative-path}
```

## <a name="access-a-group-team-site"></a><span data-ttu-id="3c7a7-127">Obtener acceso a un sitio de grupo</span><span class="sxs-lookup"><span data-stu-id="3c7a7-127">Access a group team site</span></span>

<span data-ttu-id="3c7a7-128">Para obtener acceso al sitio de grupo para un [group](../resources/group.md):</span><span class="sxs-lookup"><span data-stu-id="3c7a7-128">To access the team site for a [group](../resources/group.md):</span></span>

```http
GET /groups/{group-id}/sites/root
```

## <a name="example"></a><span data-ttu-id="3c7a7-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3c7a7-129">Example</span></span>

##### <a name="request"></a><span data-ttu-id="3c7a7-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3c7a7-130">Request</span></span>

<!-- { "blockType": "request", "name": "get-site", "scopes": "sites.read.all service.sharepoint" } -->

```http
GET https://graph.microsoft.com/v1.0/sites/{site-id}
```

##### <a name="response"></a><span data-ttu-id="3c7a7-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3c7a7-131">Response</span></span>

<!-- { "blockType": "response", "@type": "microsoft.graph.site", "truncated": true } -->

```json
HTTP/1.1 200 OK
Content-type: application/json

{
    "id": "d297964f-d325-424b-a002-f54048a4622e",
    "name": "OneDrive / SharePoint Team",
    "description": "Collaboration site for the OneDrive and SharePoint team",
}
```

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Site/Get site by ID"
} -->
