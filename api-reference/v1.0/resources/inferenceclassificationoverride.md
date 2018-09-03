# <a name="inferenceclassificationoverride-resource-type"></a><span data-ttu-id="bb68e-101">Tipo de recurso inferenceClassificationOverride</span><span class="sxs-lookup"><span data-stu-id="bb68e-101">inferenceClassificationOverride resource type</span></span>

<span data-ttu-id="bb68e-102">Representa el reemplazo de un usuario sobre cómo se deben clasificar siempre los mensajes entrantes de un remitente determinado.</span><span class="sxs-lookup"><span data-stu-id="bb68e-102">Represents a user's override for how incoming messages from a specific sender should always be classified as.</span></span>


## <a name="methods"></a><span data-ttu-id="bb68e-103">Métodos</span><span class="sxs-lookup"><span data-stu-id="bb68e-103">Methods</span></span>

| <span data-ttu-id="bb68e-104">Método</span><span class="sxs-lookup"><span data-stu-id="bb68e-104">Method</span></span>           | <span data-ttu-id="bb68e-105">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb68e-105">Return Type</span></span>    |<span data-ttu-id="bb68e-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb68e-106">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="bb68e-107">Update</span><span class="sxs-lookup"><span data-stu-id="bb68e-107">Update</span></span>](../api/inferenceclassificationoverride_update.md) | [<span data-ttu-id="bb68e-108">inferenceClassificationOverride</span><span class="sxs-lookup"><span data-stu-id="bb68e-108">inferenceClassificationOverride</span></span>](inferenceclassificationoverride.md) |<span data-ttu-id="bb68e-109">Cambie el campo **ClassifyAs** de una invalidación tal y como se especifica.</span><span class="sxs-lookup"><span data-stu-id="bb68e-109">Change the **classifyAs** field of an override as specified.</span></span> |
|[<span data-ttu-id="bb68e-110">Delete</span><span class="sxs-lookup"><span data-stu-id="bb68e-110">Delete</span></span>](../api/inferenceclassificationoverride_delete.md) | <span data-ttu-id="bb68e-111">Ninguno</span><span class="sxs-lookup"><span data-stu-id="bb68e-111">None</span></span> |<span data-ttu-id="bb68e-112">Elimina un reemplazo especificado por su identificador.</span><span class="sxs-lookup"><span data-stu-id="bb68e-112">Delete an override specified by its ID.</span></span> |

## <a name="properties"></a><span data-ttu-id="bb68e-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bb68e-113">Properties</span></span>
| <span data-ttu-id="bb68e-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bb68e-114">Property</span></span>     | <span data-ttu-id="bb68e-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="bb68e-115">Type</span></span>   |<span data-ttu-id="bb68e-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb68e-116">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="bb68e-117">classifyAs</span><span class="sxs-lookup"><span data-stu-id="bb68e-117">classifyAs</span></span>|<span data-ttu-id="bb68e-118">inferenceClassificationType</span><span class="sxs-lookup"><span data-stu-id="bb68e-118">InferenceClassificationType</span></span>| <span data-ttu-id="bb68e-119">Especifica cómo se deben clasificar siempre los mensajes entrantes de un remitente determinado.</span><span class="sxs-lookup"><span data-stu-id="bb68e-119">Specifies how incoming messages from a specific sender should always be classified as. Possible values are: , .</span></span> <span data-ttu-id="bb68e-120">Los valores posibles son: `focused` y `other`.</span><span class="sxs-lookup"><span data-stu-id="bb68e-120">The possible values are:</span></span>|
|<span data-ttu-id="bb68e-121">id</span><span class="sxs-lookup"><span data-stu-id="bb68e-121">id</span></span>|<span data-ttu-id="bb68e-122">cadena</span><span class="sxs-lookup"><span data-stu-id="bb68e-122">string</span></span>| <span data-ttu-id="bb68e-p102">Identificador único del reemplazo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bb68e-p102">The unique identifier of the override. Read-only.</span></span>|
|<span data-ttu-id="bb68e-125">senderEmailAddress</span><span class="sxs-lookup"><span data-stu-id="bb68e-125">senderEmailAddress</span></span>|[<span data-ttu-id="bb68e-126">emailAddress</span><span class="sxs-lookup"><span data-stu-id="bb68e-126">emailAddress</span></span>](emailaddress.md)|<span data-ttu-id="bb68e-127">Información de la dirección de correo del remitente para el que se creó la invalidación.</span><span class="sxs-lookup"><span data-stu-id="bb68e-127">The email address information of the sender for whom the override is created.</span></span>|

## <a name="relationships"></a><span data-ttu-id="bb68e-128">Relaciones</span><span class="sxs-lookup"><span data-stu-id="bb68e-128">Relationships</span></span>
<span data-ttu-id="bb68e-129">Ninguno</span><span class="sxs-lookup"><span data-stu-id="bb68e-129">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="bb68e-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="bb68e-130">JSON representation</span></span>

<span data-ttu-id="bb68e-131">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="bb68e-131">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.inferenceClassificationOverride"
}-->

```json
{
  "classifyAs": "string",
  "id": "string (identifier)",
  "senderEmailAddress": {"@odata.type": "microsoft.graph.emailAddress"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "inferenceClassificationOverride resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->