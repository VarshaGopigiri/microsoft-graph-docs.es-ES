# <a name="educationstudent-resource-type"></a><span data-ttu-id="63a9e-101">Tipo de recurso educationStudent</span><span class="sxs-lookup"><span data-stu-id="63a9e-101">educationStudent resource type</span></span>

<span data-ttu-id="63a9e-102">Información adicional que se agrega a un [educationUser](educationuser.md) que se presenta cuando el primaryRole de un usuario es `student`.</span><span class="sxs-lookup"><span data-stu-id="63a9e-102">Additional information added to an [educationUser](educationuser.md) that is present when the primaryRole of a user is `student`.</span></span>

## <a name="properties"></a><span data-ttu-id="63a9e-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="63a9e-103">Properties</span></span>
| <span data-ttu-id="63a9e-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="63a9e-104">Property</span></span>     | <span data-ttu-id="63a9e-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="63a9e-105">Type</span></span>   |<span data-ttu-id="63a9e-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="63a9e-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="63a9e-107">birthDate</span><span class="sxs-lookup"><span data-stu-id="63a9e-107">birthDate</span></span>|<span data-ttu-id="63a9e-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="63a9e-108">Date</span></span>| <span data-ttu-id="63a9e-109">Fecha de nacimiento del alumno.</span><span class="sxs-lookup"><span data-stu-id="63a9e-109">Birth date of the student.</span></span>|
|<span data-ttu-id="63a9e-110">externalId</span><span class="sxs-lookup"><span data-stu-id="63a9e-110">externalId</span></span>|<span data-ttu-id="63a9e-111">Cadena</span><span class="sxs-lookup"><span data-stu-id="63a9e-111">String</span></span>| <span data-ttu-id="63a9e-112">Identificador del alumno en el sistema de origen.</span><span class="sxs-lookup"><span data-stu-id="63a9e-112">ID of the student in the source system.</span></span>|
|<span data-ttu-id="63a9e-113">gender</span><span class="sxs-lookup"><span data-stu-id="63a9e-113">gender</span></span>|<span data-ttu-id="63a9e-114">educationGender</span><span class="sxs-lookup"><span data-stu-id="63a9e-114">educationGender values</span></span>| <span data-ttu-id="63a9e-115">Los valores posibles son: `female`, `male`, `other` y `unknownFutureValue`.</span><span class="sxs-lookup"><span data-stu-id="63a9e-115">The possible values are `female`, `male`, `other`, `unknownFutureValue`, , , , , , , , or .</span></span>|
|<span data-ttu-id="63a9e-116">grade</span><span class="sxs-lookup"><span data-stu-id="63a9e-116">grade</span></span>|<span data-ttu-id="63a9e-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="63a9e-117">String</span></span>|<span data-ttu-id="63a9e-118">Curso actual del alumno.</span><span class="sxs-lookup"><span data-stu-id="63a9e-118">Current grade level of the student.</span></span>|
|<span data-ttu-id="63a9e-119">graduationYear</span><span class="sxs-lookup"><span data-stu-id="63a9e-119">graduationYear</span></span>|<span data-ttu-id="63a9e-120">Cadena</span><span class="sxs-lookup"><span data-stu-id="63a9e-120">String</span></span>| <span data-ttu-id="63a9e-121">Año de graduación del alumno en el centro educativo.</span><span class="sxs-lookup"><span data-stu-id="63a9e-121">Year the student is graduating from the school.</span></span>|
|<span data-ttu-id="63a9e-122">studentNumber</span><span class="sxs-lookup"><span data-stu-id="63a9e-122">studentNumber</span></span>|<span data-ttu-id="63a9e-123">Cadena</span><span class="sxs-lookup"><span data-stu-id="63a9e-123">String</span></span>| <span data-ttu-id="63a9e-124">Número de alumno.</span><span class="sxs-lookup"><span data-stu-id="63a9e-124">Student Number.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="63a9e-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="63a9e-125">JSON representation</span></span>

<span data-ttu-id="63a9e-126">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="63a9e-126">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationStudent"
}-->

```json
{
  "birthDate": "String (timestamp)",
  "externalId": "String",
  "gender": "educationGender",
  "grade": "String",
  "graduationYear": "String",
  "studentNumber": "String"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationStudent resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
