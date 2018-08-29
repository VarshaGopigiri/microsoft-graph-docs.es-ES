# <a name="baseitemversion-resource-type"></a><span data-ttu-id="c4896-101">Tipo de recurso BaseItemVersion</span><span class="sxs-lookup"><span data-stu-id="c4896-101">BaseItemVersion resource type</span></span>

<span data-ttu-id="c4896-102">El recurso **baseItemVersion** representa una versión anterior de un elemento o una entidad.</span><span class="sxs-lookup"><span data-stu-id="c4896-102">The **baseItemVersion** resource represents a previous version of an item or entity.</span></span>


## <a name="json-representation"></a><span data-ttu-id="c4896-103">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c4896-103">JSON representation</span></span>

<!--{
  "blockType": "resource",
  "abstract": true,
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.baseItemVersion",
  "@type.aka": "oneDrive.baseItemVersion"
}-->

```json
{
  "id": "string",
  "lastModifiedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "lastModifiedDateTime": "2016-01-01T15:20:01.125Z",
  "publication": { "@odata.type": "microsoft.graph.publicationFacet" }
}
```

## <a name="properties"></a><span data-ttu-id="c4896-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c4896-104">Properties</span></span>

|      <span data-ttu-id="c4896-105">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="c4896-105">Property name</span></span>       |                         <span data-ttu-id="c4896-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="c4896-106">Type</span></span>                         |                               <span data-ttu-id="c4896-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4896-107">Description</span></span>                               |
| :----------------------- | :--------------------------------------------------- | :---------------------------------------------------------------------- |
| <span data-ttu-id="c4896-108">**id**</span><span class="sxs-lookup"><span data-stu-id="c4896-108">**id**</span></span>                   | <span data-ttu-id="c4896-109">cadena</span><span class="sxs-lookup"><span data-stu-id="c4896-109">string</span></span>                                               | <span data-ttu-id="c4896-110">El identificador de la versión.</span><span class="sxs-lookup"><span data-stu-id="c4896-110">The ID of the version.</span></span> <span data-ttu-id="c4896-111">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c4896-111">Read-only.</span></span>                                       |
| <span data-ttu-id="c4896-112">**lastModifiedBy**</span><span class="sxs-lookup"><span data-stu-id="c4896-112">**lastModifiedBy**</span></span>       | [<span data-ttu-id="c4896-113">IdentitySet</span><span class="sxs-lookup"><span data-stu-id="c4896-113">IdentitySet</span></span>](../resources/identitySet.md)           | <span data-ttu-id="c4896-114">Identidad del usuario que modificó por última vez la versión.</span><span class="sxs-lookup"><span data-stu-id="c4896-114">Identity of the user which last modified the version.</span></span> <span data-ttu-id="c4896-115">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c4896-115">Read-only.</span></span>        |
| <span data-ttu-id="c4896-116">**lastModifiedDateTime**</span><span class="sxs-lookup"><span data-stu-id="c4896-116">**lastModifiedDateTime**</span></span> | [<span data-ttu-id="c4896-117">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c4896-117">DateTimeOffset</span></span>](../resources/timestamp.md)          | <span data-ttu-id="c4896-118">Fecha y hora de la última modificación de la versión.</span><span class="sxs-lookup"><span data-stu-id="c4896-118">Date and time the version was last modified.</span></span> <span data-ttu-id="c4896-119">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c4896-119">Read-only.</span></span>                 |
| <span data-ttu-id="c4896-120">**publication**</span><span class="sxs-lookup"><span data-stu-id="c4896-120">**publication**</span></span>          | [<span data-ttu-id="c4896-121">PublicationFacet</span><span class="sxs-lookup"><span data-stu-id="c4896-121">PublicationFacet</span></span>](../resources/publicationfacet.md) | <span data-ttu-id="c4896-122">Indica el estado de publicación de esta versión concreta.</span><span class="sxs-lookup"><span data-stu-id="c4896-122">Indicates the publication status of this particular version.</span></span> <span data-ttu-id="c4896-123">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c4896-123">Read-only.</span></span> |


<!-- {
  "type": "#page.annotation",
  "description": "The version facet provides information about the properties of a file version.",
  "keywords": "version,versions,version-history,history",
  "section": "documentation",
  "tocPath": "Facets/Version"
} -->
