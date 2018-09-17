# <a name="alerttrigger-resource-type"></a><span data-ttu-id="40a8a-101">Tipo de recurso alertTrigger</span><span class="sxs-lookup"><span data-stu-id="40a8a-101">alertTrigger resource type</span></span>

<span data-ttu-id="40a8a-102">Contiene información acerca de las propiedades que han desencadenado una detección (propiedades que existen en la entidad de alerta).</span><span class="sxs-lookup"><span data-stu-id="40a8a-102">Contains information about the properties that triggered a detection (properties exist in the alert entity).</span></span>

## <a name="properties"></a><span data-ttu-id="40a8a-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="40a8a-103">Properties</span></span>

| <span data-ttu-id="40a8a-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="40a8a-104">Property</span></span>   | <span data-ttu-id="40a8a-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="40a8a-105">Type</span></span>|<span data-ttu-id="40a8a-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="40a8a-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="40a8a-107">nombre</span><span class="sxs-lookup"><span data-stu-id="40a8a-107">name</span></span>|<span data-ttu-id="40a8a-108">Cadena</span><span class="sxs-lookup"><span data-stu-id="40a8a-108">String</span></span>|<span data-ttu-id="40a8a-109">Nombre de la propiedad que actúa como desencadenador de la detección.</span><span class="sxs-lookup"><span data-stu-id="40a8a-109">Name of the property serving as a detection trigger.</span></span>|
|<span data-ttu-id="40a8a-110">tipo</span><span class="sxs-lookup"><span data-stu-id="40a8a-110">type</span></span>|<span data-ttu-id="40a8a-111">Cadena</span><span class="sxs-lookup"><span data-stu-id="40a8a-111">String</span></span>|<span data-ttu-id="40a8a-112">Tipo de la propiedad en el par key:value para interpretación.</span><span class="sxs-lookup"><span data-stu-id="40a8a-112">Type of the property in the key:value pair for interpretation.</span></span> <span data-ttu-id="40a8a-113">Por ejemplo, Cadena, Booleano, etc.</span><span class="sxs-lookup"><span data-stu-id="40a8a-113">For example, String, Boolean, etc.</span></span>|
|<span data-ttu-id="40a8a-114">valor</span><span class="sxs-lookup"><span data-stu-id="40a8a-114">value</span></span>|<span data-ttu-id="40a8a-115">Cadena</span><span class="sxs-lookup"><span data-stu-id="40a8a-115">String</span></span>|<span data-ttu-id="40a8a-116">Valor de la propiedad que actúa como desencadenador de la detección.</span><span class="sxs-lookup"><span data-stu-id="40a8a-116">Value of the property serving as a detection trigger.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="40a8a-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="40a8a-117">JSON representation</span></span>

<span data-ttu-id="40a8a-118">Esta es una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="40a8a-118">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.alertTrigger"
}-->

```json
{
  "name": "String",
  "type": "String",
  "value": "String"
}

```

## <a name="example"></a><span data-ttu-id="40a8a-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="40a8a-119">Example</span></span>

```json
{
  "name": "endpointAddress",
  "type": "networkConnection.sourceAddress",
  "value": "10.154.9.40"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "alertTrigger resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->