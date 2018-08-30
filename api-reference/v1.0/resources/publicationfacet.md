# <a name="publicationfacet-resource-type"></a><span data-ttu-id="3e5ab-101">Tipo de recurso PublicationFacet</span><span class="sxs-lookup"><span data-stu-id="3e5ab-101">PublicationFacet resource type</span></span>

<span data-ttu-id="3e5ab-102">El recurso **publicationFacet** proporciona información detallada sobre el estado publicado de un recurso [driveItemVersion](driveitemversion.md) o [driveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="3e5ab-102">The **publicationFacet** resource provides details on the published status of a [driveItemVersion](driveitemversion.md) or [driveItem](driveitem.md) resource.</span></span>

## <a name="json-representation"></a><span data-ttu-id="3e5ab-103">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3e5ab-103">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [  ],
  "@odata.type": "microsoft.graph.publicationFacet"
}-->

```json
{
  "level": "published | checkout",
  "versionId": "string"
}
```

## <a name="properties"></a><span data-ttu-id="3e5ab-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3e5ab-104">Properties</span></span>

|   <span data-ttu-id="3e5ab-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3e5ab-105">Property</span></span>    |  <span data-ttu-id="3e5ab-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="3e5ab-106">Type</span></span>  | <span data-ttu-id="3e5ab-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="3e5ab-107">Description</span></span> |
| :------------ | :----- | :---------- |
| <span data-ttu-id="3e5ab-108">**level**</span><span class="sxs-lookup"><span data-stu-id="3e5ab-108">**level**</span></span>     | <span data-ttu-id="3e5ab-109">Cadena</span><span class="sxs-lookup"><span data-stu-id="3e5ab-109">String</span></span> | <span data-ttu-id="3e5ab-110">El estado de publicación de este documento.</span><span class="sxs-lookup"><span data-stu-id="3e5ab-110">The state of publication for this document.</span></span> <span data-ttu-id="3e5ab-111">o `checkout`.`published`</span><span class="sxs-lookup"><span data-stu-id="3e5ab-111">Either `published` or `checkout`.</span></span> <span data-ttu-id="3e5ab-112">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3e5ab-112">Read-only.</span></span>  |
| <span data-ttu-id="3e5ab-113">**versionId**</span><span class="sxs-lookup"><span data-stu-id="3e5ab-113">**versionId**</span></span> | <span data-ttu-id="3e5ab-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="3e5ab-114">String</span></span> | <span data-ttu-id="3e5ab-115">El identificador único de la versión que está visible para el llamador actual.</span><span class="sxs-lookup"><span data-stu-id="3e5ab-115">The unique identifier for the version that is visible to the current caller.</span></span> <span data-ttu-id="3e5ab-116">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3e5ab-116">Read-only.</span></span>  |


<!-- {
  "type": "#page.annotation",
  "description": "The photo facet provides details about the camera and settings on the camera for photos.",
  "keywords": "camera make,camera model, exposure, f-stop, iso",
  "section": "documentation",
  "suppressions": [
    " Warning: /api-reference/v1.0/resources/publicationfacet.md:
      Found potential enums in resource example that weren't defined in a table:(published,checkout) are in resource, but () are in table"
  ],
  "tocPath": "Facets/Photo"
} -->
