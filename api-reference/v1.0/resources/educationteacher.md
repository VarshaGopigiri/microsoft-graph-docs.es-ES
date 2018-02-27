# <a name="educationteacher-resource-type"></a><span data-ttu-id="6f9dd-101">Tipo de recurso educationTeacher</span><span class="sxs-lookup"><span data-stu-id="6f9dd-101">educationTeacher resource type</span></span>

<span data-ttu-id="6f9dd-102">Información adicional que se agrega a un [educationUser](educationuser.md) que se presenta cuando el primaryRole de un usuario es `teacher`.</span><span class="sxs-lookup"><span data-stu-id="6f9dd-102">Additional information added to an [educationUser](educationuser.md) that is present when the primaryRole of a user is `teacher`.</span></span>


## <a name="properties"></a><span data-ttu-id="6f9dd-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6f9dd-103">Properties</span></span>
| <span data-ttu-id="6f9dd-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6f9dd-104">Property</span></span>     | <span data-ttu-id="6f9dd-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="6f9dd-105">Type</span></span>   |<span data-ttu-id="6f9dd-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f9dd-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6f9dd-107">externalId</span><span class="sxs-lookup"><span data-stu-id="6f9dd-107">externalId</span></span>|<span data-ttu-id="6f9dd-108">String</span><span class="sxs-lookup"><span data-stu-id="6f9dd-108">String</span></span>| <span data-ttu-id="6f9dd-109">Identificador del profesor en el sistema de origen.</span><span class="sxs-lookup"><span data-stu-id="6f9dd-109">ID of the teacher in the source system.</span></span>|
|<span data-ttu-id="6f9dd-110">teacherNumber</span><span class="sxs-lookup"><span data-stu-id="6f9dd-110">teacherNumber</span></span>|<span data-ttu-id="6f9dd-111">String</span><span class="sxs-lookup"><span data-stu-id="6f9dd-111">String</span></span>|<span data-ttu-id="6f9dd-112">Número de profesor</span><span class="sxs-lookup"><span data-stu-id="6f9dd-112">Teacher number.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="6f9dd-113">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6f9dd-113">JSON representation</span></span>

<span data-ttu-id="6f9dd-114">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="6f9dd-114">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationTeacher"
}-->

```json
{
  "externalId": "String",
  "teacherNumber": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationTeacher resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->