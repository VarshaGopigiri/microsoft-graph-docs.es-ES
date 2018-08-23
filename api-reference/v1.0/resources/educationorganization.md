# <a name="educationorganization-resource-type"></a><span data-ttu-id="53ad6-101">Tipo de recurso educationOrganization</span><span class="sxs-lookup"><span data-stu-id="53ad6-101">educationOrganization resource type</span></span>

<span data-ttu-id="53ad6-102">Entidad abstracta que se utiliza para modelar la uniformidad entre los diferentes tipos de organización en el sector de la educación.</span><span class="sxs-lookup"><span data-stu-id="53ad6-102">Abstract entity used to model the commonality between different organization types within the education sector.</span></span>

## <a name="properties"></a><span data-ttu-id="53ad6-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="53ad6-103">Properties</span></span>
| <span data-ttu-id="53ad6-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="53ad6-104">Property</span></span>     | <span data-ttu-id="53ad6-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="53ad6-105">Type</span></span>   |<span data-ttu-id="53ad6-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="53ad6-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="53ad6-107">description</span><span class="sxs-lookup"><span data-stu-id="53ad6-107">description</span></span>|<span data-ttu-id="53ad6-108">Cadena</span><span class="sxs-lookup"><span data-stu-id="53ad6-108">String</span></span>| <span data-ttu-id="53ad6-109">Descripción de la organización.</span><span class="sxs-lookup"><span data-stu-id="53ad6-109">Organization description.</span></span>|
|<span data-ttu-id="53ad6-110">displayName</span><span class="sxs-lookup"><span data-stu-id="53ad6-110">displayName</span></span>|<span data-ttu-id="53ad6-111">Cadena</span><span class="sxs-lookup"><span data-stu-id="53ad6-111">String</span></span>| <span data-ttu-id="53ad6-112">Nombre para mostrar de organización.</span><span class="sxs-lookup"><span data-stu-id="53ad6-112">Organization display name.</span></span>|
|<span data-ttu-id="53ad6-113">externalSource</span><span class="sxs-lookup"><span data-stu-id="53ad6-113">externalSource</span></span>|<span data-ttu-id="53ad6-114">educationExternalSource</span><span class="sxs-lookup"><span data-stu-id="53ad6-114">educationExternalSource</span></span>| <span data-ttu-id="53ad6-115">Origen desde el que se creó esta organización.</span><span class="sxs-lookup"><span data-stu-id="53ad6-115">Source where this organization was created from.</span></span> <span data-ttu-id="53ad6-116">Los valores posibles son: `sis`, `manual` y `unknownFutureValue`.</span><span class="sxs-lookup"><span data-stu-id="53ad6-116">The possible values are:</span></span>|

## <a name="relationships"></a><span data-ttu-id="53ad6-117">Relaciones</span><span class="sxs-lookup"><span data-stu-id="53ad6-117">Relationships</span></span>
<span data-ttu-id="53ad6-118">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="53ad6-118">None.</span></span>


## <a name="json-representation"></a><span data-ttu-id="53ad6-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="53ad6-119">JSON representation</span></span>

<span data-ttu-id="53ad6-120">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="53ad6-120">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "abstract": true,
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationOrganization"
}-->

```json
{
  "description": "String",
  "displayName": "String",
  "externalSource": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationOrganization resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->