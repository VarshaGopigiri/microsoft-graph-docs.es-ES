# <a name="sharinglink-resource-type"></a><span data-ttu-id="f68d3-101">Tipo de recurso SharingLink</span><span class="sxs-lookup"><span data-stu-id="f68d3-101">SharingLink resource type</span></span>

<span data-ttu-id="f68d3-102">El recurso **SharingLink** agrupa en una sola estructura los elementos de datos relacionados con vínculos.</span><span class="sxs-lookup"><span data-stu-id="f68d3-102">The **SharingLink** resource groups link-related data items into a single structure.</span></span>

<span data-ttu-id="f68d3-103">Si un recurso [**Permission**](permission.md) tiene una faceta **sharingLink** que no es NULL, el permiso representa un vínculo para compartir (a diferencia de los permisos concedidos a una persona o un grupo).</span><span class="sxs-lookup"><span data-stu-id="f68d3-103">If a [**Permission**](permission.md) resource has a non-null **sharingLink** facet, the permission represents a sharing link (as opposed to permissions granted to a person or group).</span></span>

## <a name="json-representation"></a><span data-ttu-id="f68d3-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f68d3-104">JSON representation</span></span>

<span data-ttu-id="f68d3-105">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f68d3-105">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [ "application", "scope" ],
  "@odata.type": "microsoft.graph.sharingLink"
}-->

```json
{
  "application": {"@odata.type": "microsoft.graph.identity"},
  "type": "view | edit",
  "scope": "anonymous | organization",
  "webUrl": "url"
}
```

## <a name="properties"></a><span data-ttu-id="f68d3-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f68d3-106">Properties</span></span>

| <span data-ttu-id="f68d3-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f68d3-107">Property</span></span>    | <span data-ttu-id="f68d3-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="f68d3-108">Type</span></span>                    | <span data-ttu-id="f68d3-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f68d3-109">Description</span></span>                                                                                                                                                                                             |
|:------------|:------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f68d3-110">application</span><span class="sxs-lookup"><span data-stu-id="f68d3-110">application</span></span> | [<span data-ttu-id="f68d3-111">identity</span><span class="sxs-lookup"><span data-stu-id="f68d3-111">identity</span></span>](identity.md) | <span data-ttu-id="f68d3-112">La aplicación con la que está asociada el vínculo.</span><span class="sxs-lookup"><span data-stu-id="f68d3-112">The app the link is associated with.</span></span>                                                                                                                                                                    |
| <span data-ttu-id="f68d3-113">type</span><span class="sxs-lookup"><span data-stu-id="f68d3-113">type</span></span>        | <span data-ttu-id="f68d3-114">String</span><span class="sxs-lookup"><span data-stu-id="f68d3-114">String</span></span>                  | <span data-ttu-id="f68d3-115">El tipo del vínculo creado.</span><span class="sxs-lookup"><span data-stu-id="f68d3-115">The type of the link created.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="f68d3-116">scope</span><span class="sxs-lookup"><span data-stu-id="f68d3-116">scope</span></span>       | <span data-ttu-id="f68d3-117">String</span><span class="sxs-lookup"><span data-stu-id="f68d3-117">String</span></span>                  | <span data-ttu-id="f68d3-p101">El ámbito del vínculo representado por este permiso. El valor `anonymous` indica que cualquier usuario puede usar el vínculo, `organization` indica que solo pueden usar el vínculo los usuarios que han iniciado sesión en el mismo inquilino.</span><span class="sxs-lookup"><span data-stu-id="f68d3-p101">The scope of the link represented by this permission. Value `anonymous` indicates the link is usable by anyone, `organization` indicates the link is only usable for users signed into the same tenant.</span></span> |
| <span data-ttu-id="f68d3-120">webUrl</span><span class="sxs-lookup"><span data-stu-id="f68d3-120">webUrl</span></span>      | <span data-ttu-id="f68d3-121">String</span><span class="sxs-lookup"><span data-stu-id="f68d3-121">String</span></span>                  | <span data-ttu-id="f68d3-122">Una dirección URL que abre el elemento en el explorador en el sitio web de OneDrive.</span><span class="sxs-lookup"><span data-stu-id="f68d3-122">A URL that opens the item in the browser on the OneDrive website.</span></span>                                                                                                                                       |

## <a name="type-enumeration"></a><span data-ttu-id="f68d3-123">Enumeración de tipos</span><span class="sxs-lookup"><span data-stu-id="f68d3-123">Type enumeration</span></span>

<span data-ttu-id="f68d3-124">Esta tabla define los valores posibles de la propiedad **type**:</span><span class="sxs-lookup"><span data-stu-id="f68d3-124">This table defines the possible values for the **type** property:</span></span>

| <span data-ttu-id="f68d3-125">Valor</span><span class="sxs-lookup"><span data-stu-id="f68d3-125">Value</span></span>   | <span data-ttu-id="f68d3-126">Rol</span><span class="sxs-lookup"><span data-stu-id="f68d3-126">Role</span></span>    | <span data-ttu-id="f68d3-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="f68d3-127">Description</span></span>                                                                     |
|:--------|:--------|:--------------------------------------------------------------------------------|
| `view`  | `read`  | <span data-ttu-id="f68d3-128">Un vínculo para compartir de solo vista, que permite el acceso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f68d3-128">A view-only sharing link, allowing read-only access.</span></span>                            |
| `edit`  | `write` | <span data-ttu-id="f68d3-129">Un vínculo para compartir de edición, que permite el acceso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="f68d3-129">An edit sharing link, allowing read-write access.</span></span>                               |

## <a name="scope-enumeration"></a><span data-ttu-id="f68d3-130">Enumeración del ámbito</span><span class="sxs-lookup"><span data-stu-id="f68d3-130">Scope enumeration</span></span>

| <span data-ttu-id="f68d3-131">Valor</span><span class="sxs-lookup"><span data-stu-id="f68d3-131">Value</span></span>          | <span data-ttu-id="f68d3-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="f68d3-132">Description</span></span>                                                                                                                 |
|:---------------|:----------------------------------------------------------------------------------------------------------------------------|
| `anonymous`    | <span data-ttu-id="f68d3-133">El vínculo para compartir está disponible para que lo use cualquier usuario.</span><span class="sxs-lookup"><span data-stu-id="f68d3-133">The sharing link is available for anyone to use.</span></span>                                                                            |
| `organization` | <span data-ttu-id="f68d3-p102">El vínculo para compartir está disponible para que lo use cualquier usuario de la misma organización (inquilino). No está disponible para OneDrive Personal.</span><span class="sxs-lookup"><span data-stu-id="f68d3-p102">The sharing link is available for anyone within the same organization (tenant) to use. Not available for OneDrive Personal.</span></span> |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "sharingLink resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
