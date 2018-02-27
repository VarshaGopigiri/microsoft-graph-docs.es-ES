# <a name="educationstudent-resource-type"></a><span data-ttu-id="5104b-101">Tipo de recurso educationStudent</span><span class="sxs-lookup"><span data-stu-id="5104b-101">educationStudent resource type</span></span>

<span data-ttu-id="5104b-102">Información adicional que se agrega a un [educationUser](educationuser.md) que se presenta cuando el primaryRole de un usuario es `student`.</span><span class="sxs-lookup"><span data-stu-id="5104b-102">Additional information added to an [educationUser](educationuser.md) that is present when the primaryRole of a user is `student`.</span></span>

## <a name="properties"></a><span data-ttu-id="5104b-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5104b-103">Properties</span></span>
| <span data-ttu-id="5104b-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5104b-104">Property</span></span>     | <span data-ttu-id="5104b-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="5104b-105">Type</span></span>   |<span data-ttu-id="5104b-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="5104b-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5104b-107">birthDate</span><span class="sxs-lookup"><span data-stu-id="5104b-107">birthDate</span></span>|<span data-ttu-id="5104b-108">Date</span><span class="sxs-lookup"><span data-stu-id="5104b-108">Date</span></span>| <span data-ttu-id="5104b-109">Fecha de nacimiento del alumno.</span><span class="sxs-lookup"><span data-stu-id="5104b-109">Birth date of the student.</span></span>|
|<span data-ttu-id="5104b-110">externalId</span><span class="sxs-lookup"><span data-stu-id="5104b-110">externalId</span></span>|<span data-ttu-id="5104b-111">String</span><span class="sxs-lookup"><span data-stu-id="5104b-111">String</span></span>| <span data-ttu-id="5104b-112">Identificador del alumno en el sistema de origen.</span><span class="sxs-lookup"><span data-stu-id="5104b-112">ID of the student in the source system.</span></span>|
|<span data-ttu-id="5104b-113">gender</span><span class="sxs-lookup"><span data-stu-id="5104b-113">Gender</span></span>|`educationGender enumeration`| <span data-ttu-id="5104b-114">Los valores posibles son: `female`, `male`, `other` y `unkownFutureValue`.</span><span class="sxs-lookup"><span data-stu-id="5104b-114">Possible values are: `female`, `male`, `other`, `unkownFutureValue`.</span></span>|
|<span data-ttu-id="5104b-115">grade</span><span class="sxs-lookup"><span data-stu-id="5104b-115">QuizInfoPage: grade</span></span>|<span data-ttu-id="5104b-116">String</span><span class="sxs-lookup"><span data-stu-id="5104b-116">String</span></span>|<span data-ttu-id="5104b-117">Curso actual del alumno.</span><span class="sxs-lookup"><span data-stu-id="5104b-117">Current grade level of the student.</span></span>|
|<span data-ttu-id="5104b-118">graduationYear</span><span class="sxs-lookup"><span data-stu-id="5104b-118">graduationYear</span></span>|<span data-ttu-id="5104b-119">String</span><span class="sxs-lookup"><span data-stu-id="5104b-119">String</span></span>| <span data-ttu-id="5104b-120">Año de graduación del alumno en el centro educativo.</span><span class="sxs-lookup"><span data-stu-id="5104b-120">Year the student is graduating from the school.</span></span>|
|<span data-ttu-id="5104b-121">studentNumber</span><span class="sxs-lookup"><span data-stu-id="5104b-121">studentNumber</span></span>|<span data-ttu-id="5104b-122">String</span><span class="sxs-lookup"><span data-stu-id="5104b-122">String</span></span>| <span data-ttu-id="5104b-123">Número de alumno.</span><span class="sxs-lookup"><span data-stu-id="5104b-123">Student Number.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="5104b-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5104b-124">JSON representation</span></span>

<span data-ttu-id="5104b-125">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="5104b-125">The following is a JSON representation of the resource.</span></span>

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