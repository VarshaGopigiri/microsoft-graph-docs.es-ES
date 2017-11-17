# <a name="extensionschemaproperty-resource-type"></a><span data-ttu-id="a8a58-101">Tipo de recurso extensionSchemaProperty</span><span class="sxs-lookup"><span data-stu-id="a8a58-101">extensionSchemaProperty resource type</span></span>

<span data-ttu-id="a8a58-102">Use los recursos **extensionSchemaProperty** para definir el nombre y el tipo de una propiedad como parte de una definición [schemaExtension](schemaextension.md).</span><span class="sxs-lookup"><span data-stu-id="a8a58-102">Use the **extensionSchemaProperty** resource to define a property's name and its type, as part of a [schemaExtension](schemaextension.md) definition.</span></span>


## <a name="properties"></a><span data-ttu-id="a8a58-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a8a58-103">Properties</span></span>
| <span data-ttu-id="a8a58-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a8a58-104">Property</span></span>     | <span data-ttu-id="a8a58-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="a8a58-105">Type</span></span>   |<span data-ttu-id="a8a58-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8a58-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a8a58-107">name</span><span class="sxs-lookup"><span data-stu-id="a8a58-107">name</span></span>|<span data-ttu-id="a8a58-108">Cadena</span><span class="sxs-lookup"><span data-stu-id="a8a58-108">String</span></span>| <span data-ttu-id="a8a58-109">El nombre de la propiedad fuertemente tipada definida como parte de una extensión de esquema.</span><span class="sxs-lookup"><span data-stu-id="a8a58-109">The name of the strongly-typed property defined as part of a schema extension.</span></span>|
|<span data-ttu-id="a8a58-110">tipo</span><span class="sxs-lookup"><span data-stu-id="a8a58-110">type</span></span>|<span data-ttu-id="a8a58-111">String</span><span class="sxs-lookup"><span data-stu-id="a8a58-111">String</span></span>| <span data-ttu-id="a8a58-p101">Tipo de la propiedad que se define como parte de una extensión de esquema.  Los valores permitidos son *Binary, Boolean, DateTime, Integer* y *String*.  Consulte la tabla siguiente para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="a8a58-p101">The type of the property that is defined as part of a schema extension.  Allowed values are *Binary, Boolean, DateTime, Integer* or *String*.  See the table below for more details.</span></span>|

#### <a name="supported-property-data-types"></a><span data-ttu-id="a8a58-115">Tipos de datos de propiedad admitidos</span><span class="sxs-lookup"><span data-stu-id="a8a58-115">Supported property data types</span></span> 
<span data-ttu-id="a8a58-116">Se admiten los siguientes tipos de datos al definir una propiedad en una extensión de esquema:</span><span class="sxs-lookup"><span data-stu-id="a8a58-116">The following data types are supported when defining a property in a schema extension:</span></span>

| <span data-ttu-id="a8a58-117">Tipo de propiedad</span><span class="sxs-lookup"><span data-stu-id="a8a58-117">Property Type</span></span> | <span data-ttu-id="a8a58-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8a58-118">Remarks</span></span> |
|-------------|------------|
| <span data-ttu-id="a8a58-119">Binario</span><span class="sxs-lookup"><span data-stu-id="a8a58-119">Binary</span></span> | <span data-ttu-id="a8a58-120">Máximo de 256 bytes.</span><span class="sxs-lookup"><span data-stu-id="a8a58-120">256 bytes maximum.</span></span> |
| <span data-ttu-id="a8a58-121">Boolean</span><span class="sxs-lookup"><span data-stu-id="a8a58-121">Boolean</span></span> | <span data-ttu-id="a8a58-122">No se admite para contactos, mensajes, eventos y publicaciones.</span><span class="sxs-lookup"><span data-stu-id="a8a58-122">Not supported for messages, events and posts.</span></span> |
| <span data-ttu-id="a8a58-123">DateTime</span><span class="sxs-lookup"><span data-stu-id="a8a58-123">DateTime</span></span> | <span data-ttu-id="a8a58-p102">Debe especificarse en el formato ISO 8601. Se almacenarán en UTC.</span><span class="sxs-lookup"><span data-stu-id="a8a58-p102">Must be specified in ISO 8601 format. Will be stored in UTC.</span></span> |
| <span data-ttu-id="a8a58-126">Integer</span><span class="sxs-lookup"><span data-stu-id="a8a58-126">Integer</span></span> | <span data-ttu-id="a8a58-127">Valor de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a8a58-127">A 32-bit integer value.</span></span> <span data-ttu-id="a8a58-128">No se admite para contactos, mensajes, eventos y publicaciones.</span><span class="sxs-lookup"><span data-stu-id="a8a58-128">Not supported for messages, events and posts.</span></span> |
| <span data-ttu-id="a8a58-129">String</span><span class="sxs-lookup"><span data-stu-id="a8a58-129">String</span></span> | <span data-ttu-id="a8a58-130">256 caracteres como máximo.</span><span class="sxs-lookup"><span data-stu-id="a8a58-130">256 characters maximum.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="a8a58-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a8a58-131">JSON representation</span></span>
<span data-ttu-id="a8a58-132">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a8a58-132">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.extensionSchemaProperty"
}-->

```json
{
  "name": "String",
  "type": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "extensionSchemaProperty resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
