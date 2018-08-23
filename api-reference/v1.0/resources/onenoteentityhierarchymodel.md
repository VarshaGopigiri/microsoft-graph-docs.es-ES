# <a name="onenoteentityhierarchymodel-resource"></a><span data-ttu-id="7d8a6-101">Recurso onenoteEntityHierarchyModel</span><span class="sxs-lookup"><span data-stu-id="7d8a6-101">onenoteEntityHierarchyModel resource</span></span>

<span data-ttu-id="7d8a6-102">Este es un tipo base para las entidades de OneNote.</span><span class="sxs-lookup"><span data-stu-id="7d8a6-102">This is a base type for OneNote entities.</span></span>

## <a name="json-representation"></a><span data-ttu-id="7d8a6-103">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7d8a6-103">JSON representation</span></span>

<span data-ttu-id="7d8a6-104">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7d8a6-104">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "abstract": true,
  "baseType": "microsoft.graph.onenoteEntitySchemaObjectModel",
  "optionalProperties": [
    "self"
  ],
  "@odata.type": "microsoft.graph.onenoteEntityHierarchyModel"
}-->

```json
{
  "displayName": "string",
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "lastModifiedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "lastModifiedDateTime": "String (timestamp)"
}

```
## <a name="properties"></a><span data-ttu-id="7d8a6-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7d8a6-105">Properties</span></span>
## <a name="properties"></a><span data-ttu-id="7d8a6-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7d8a6-106">Properties</span></span>
| <span data-ttu-id="7d8a6-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7d8a6-107">Property</span></span>     | <span data-ttu-id="7d8a6-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="7d8a6-108">Type</span></span>   |<span data-ttu-id="7d8a6-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="7d8a6-109">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7d8a6-110">displayName</span><span class="sxs-lookup"><span data-stu-id="7d8a6-110">displayName</span></span>|<span data-ttu-id="7d8a6-111">Cadena</span><span class="sxs-lookup"><span data-stu-id="7d8a6-111">String</span></span>|<span data-ttu-id="7d8a6-112">El nombre del bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="7d8a6-112">The name of the notebook.</span></span>|
|<span data-ttu-id="7d8a6-113">createdBy</span><span class="sxs-lookup"><span data-stu-id="7d8a6-113">createdBy</span></span>|[<span data-ttu-id="7d8a6-114">identitySet</span><span class="sxs-lookup"><span data-stu-id="7d8a6-114">identitySet</span></span>](identityset.md)|<span data-ttu-id="7d8a6-p101">Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7d8a6-p101">Identity of the user, device, and application which created the item. Read-only.</span></span>|
|<span data-ttu-id="7d8a6-117">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="7d8a6-117">lastModifiedBy</span></span>|[<span data-ttu-id="7d8a6-118">identitySet</span><span class="sxs-lookup"><span data-stu-id="7d8a6-118">identitySet</span></span>](identityset.md)|<span data-ttu-id="7d8a6-p102">Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7d8a6-p102">Identity of the user, device, and application which created the item. Read-only.</span></span>|
|<span data-ttu-id="7d8a6-121">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="7d8a6-121">lastModifiedDateTime</span></span>|<span data-ttu-id="7d8a6-122">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7d8a6-122">DateTimeOffset</span></span>|<span data-ttu-id="7d8a6-p103">La fecha y la hora en que se modificó por última vez el bloc de notas. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7d8a6-p103">The date and time when the notebook was last modified. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.</span></span>|

<!-- uuid: 8b1af557-1a7c-4432-86eb-94989c2d4b54
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "page resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->