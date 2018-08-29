# <a name="profilephoto-resource-type"></a><span data-ttu-id="3d5bb-101">Tipo de recurso profilePhoto</span><span class="sxs-lookup"><span data-stu-id="3d5bb-101">profilePhoto resource type</span></span>
<span data-ttu-id="3d5bb-p101">Foto de perfil de un usuario, grupo o un contacto de Outlook al que se accede desde Exchange Online. Son datos binarios no codificados en base 64.</span><span class="sxs-lookup"><span data-stu-id="3d5bb-p101">A profile photo of a user, group or an Outlook contact accessed from Exchange Online. It's binary data not encoded in base-64.</span></span>

<span data-ttu-id="3d5bb-104">Los tamaños de fotos HD admitidos en Exchange Online son los siguientes: '48x48', '64x64', '96x96', '120x120', '240x240', '360x360','432x432', '504x504' y '648x648'.</span><span class="sxs-lookup"><span data-stu-id="3d5bb-104">The supported sizes of HD photos on Exchange Online are as follows: '48x48', '64x64', '96x96', '120x120', '240x240', '360x360','432x432', '504x504', and '648x648'.</span></span> 

## <a name="methods"></a><span data-ttu-id="3d5bb-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="3d5bb-105">Methods</span></span>

| <span data-ttu-id="3d5bb-106">Método</span><span class="sxs-lookup"><span data-stu-id="3d5bb-106">Method</span></span>       | <span data-ttu-id="3d5bb-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3d5bb-107">Return Type</span></span>  |<span data-ttu-id="3d5bb-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="3d5bb-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="3d5bb-109">Get profilePhoto</span><span class="sxs-lookup"><span data-stu-id="3d5bb-109">Get profilePhoto</span></span>](../api/profilephoto_get.md) | [<span data-ttu-id="3d5bb-110">profilePhoto</span><span class="sxs-lookup"><span data-stu-id="3d5bb-110">profilePhoto</span></span>](profilephoto.md) |<span data-ttu-id="3d5bb-111">Obtiene el **profilePhoto** especificado o sus metadatos (propiedades profilePhoto).</span><span class="sxs-lookup"><span data-stu-id="3d5bb-111">Get the specified **profilePhoto** or its metadata (profilePhoto properties).</span></span>|
|[<span data-ttu-id="3d5bb-112">Update</span><span class="sxs-lookup"><span data-stu-id="3d5bb-112">Update</span></span>](../api/profilephoto_update.md) | [<span data-ttu-id="3d5bb-113">profilePhoto</span><span class="sxs-lookup"><span data-stu-id="3d5bb-113">profilePhoto</span></span>](profilephoto.md)  |<span data-ttu-id="3d5bb-p102">Asigna una foto al usuario, grupo o contacto que se especifique. La foto debe estar en formato binario. Reemplaza la foto existente, si existe.</span><span class="sxs-lookup"><span data-stu-id="3d5bb-p102">Assign a photo to the specified user, group, or contact. The photo should be in binary. It replaces the existing photo, if any.</span></span>|

## <a name="properties"></a><span data-ttu-id="3d5bb-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3d5bb-117">Properties</span></span>
| <span data-ttu-id="3d5bb-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3d5bb-118">Property</span></span>     | <span data-ttu-id="3d5bb-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="3d5bb-119">Type</span></span>   |<span data-ttu-id="3d5bb-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="3d5bb-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="3d5bb-121">id</span><span class="sxs-lookup"><span data-stu-id="3d5bb-121">id</span></span>|<span data-ttu-id="3d5bb-122">string</span><span class="sxs-lookup"><span data-stu-id="3d5bb-122">string</span></span>|<span data-ttu-id="3d5bb-123">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3d5bb-123">Read-only.</span></span>|
|<span data-ttu-id="3d5bb-124">height</span><span class="sxs-lookup"><span data-stu-id="3d5bb-124">height</span></span>|<span data-ttu-id="3d5bb-125">int32</span><span class="sxs-lookup"><span data-stu-id="3d5bb-125">int32</span></span>|<span data-ttu-id="3d5bb-p103">Alto de la foto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3d5bb-p103">The height of the photo. Read-only.</span></span>|
|<span data-ttu-id="3d5bb-128">width</span><span class="sxs-lookup"><span data-stu-id="3d5bb-128">width</span></span>|<span data-ttu-id="3d5bb-129">int32</span><span class="sxs-lookup"><span data-stu-id="3d5bb-129">int32</span></span>|<span data-ttu-id="3d5bb-p104">Ancho de la foto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3d5bb-p104">The width of the photo. Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="3d5bb-132">Relaciones</span><span class="sxs-lookup"><span data-stu-id="3d5bb-132">Relationships</span></span>
<span data-ttu-id="3d5bb-133">Ninguno</span><span class="sxs-lookup"><span data-stu-id="3d5bb-133">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="3d5bb-134">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3d5bb-134">JSON representation</span></span>

<span data-ttu-id="3d5bb-135">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="3d5bb-135">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [],
  "isMediaEntity": true,
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.profilePhoto"
}-->

```json
{
  "id": "240X240",
  "height": 240,
  "width": 240
}

```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "profilePhoto resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
