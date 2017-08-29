# <a name="enumerate-subsites-of-a-site"></a><span data-ttu-id="e6d98-101">Enumerar los subsitios de un sitio</span><span class="sxs-lookup"><span data-stu-id="e6d98-101">Enumerate subsites of a site</span></span>

<span data-ttu-id="e6d98-102">Obtener una colección de subsitios definidos para un [sitio][].</span><span class="sxs-lookup"><span data-stu-id="e6d98-102">Get a collection of subsites defined for a [site][].</span></span>

<span data-ttu-id="e6d98-103">[sitio]: ../resources/site.md</span><span class="sxs-lookup"><span data-stu-id="e6d98-103">[site]: ../resources/site.md</span></span>

## <a name="permissions"></a><span data-ttu-id="e6d98-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="e6d98-104">Permissions</span></span>

<span data-ttu-id="e6d98-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="e6d98-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="e6d98-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e6d98-107">Permission type</span></span>      | <span data-ttu-id="e6d98-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e6d98-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e6d98-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e6d98-109">Delegated (work or school account)</span></span> | <span data-ttu-id="e6d98-110">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e6d98-110">Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="e6d98-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e6d98-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e6d98-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e6d98-112">Not supported.</span></span>    |
|<span data-ttu-id="e6d98-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e6d98-113">Application</span></span> | <span data-ttu-id="e6d98-114">Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e6d98-114">Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="e6d98-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e6d98-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /sites/{site-id}/sites
```

## <a name="example"></a><span data-ttu-id="e6d98-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e6d98-116">Example</span></span>

#### <a name="request"></a><span data-ttu-id="e6d98-117">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e6d98-117">Request</span></span>

<!-- { "blockType": "request", "name": "list-subsites" } -->

```http
GET /sites/{site-id}/sites
```

#### <a name="response"></a><span data-ttu-id="e6d98-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e6d98-118">Response</span></span>

<!-- { "blockType": "response", "@type": "microsoft.graph.site", "isCollection": true, "truncated": true } -->

```json
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "id": "da60e844-ba1d-49bc-b4d4-d5e36bae9019,712a596e-90a1-49e3-9b48-bfa80bee8740",
      "name": "Team A Subsite",
      "description": "",
      "createdDateTime": "2016-10-18T03:05:59Z",
      "lastModifiedDateTime": "2016-10-18T10:40:59Z",
      "webUrl": "https://contoso.sharepoint.com/sites/site/subsiteA"
    },
    {
      "id": "da60e844-ba1d-49bc-b4d4-d5e36bae9019,0271110f-634f-4300-a841-3a8a2e851851",
      "name": "Team B Subsite",
      "description": "",
      "createdDateTime": "2016-10-18T03:05:59Z",
      "lastModifiedDateTime": "2016-10-18T10:40:59Z",
      "webUrl": "https://contoso.sharepoint.com/sites/site/subsiteB"
    }
  ]
}
```

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Site/Enumerate subsites"
} -->
