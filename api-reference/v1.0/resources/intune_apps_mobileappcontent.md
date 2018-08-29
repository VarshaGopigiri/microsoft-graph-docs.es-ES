# <a name="mobileappcontent-resource-type"></a><span data-ttu-id="00683-101">Tipo de recurso mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="00683-101">mobileAppContent resource type</span></span>

> <span data-ttu-id="00683-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="00683-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="00683-103">Contiene las propiedades del contenido de una versión de aplicación específica.</span><span class="sxs-lookup"><span data-stu-id="00683-103">Contains content properties for a specific app version.</span></span> <span data-ttu-id="00683-104">Cada mobileAppContent puede tener varios mobileAppContentFile.</span><span class="sxs-lookup"><span data-stu-id="00683-104">Each mobileAppContent can have multiple mobileAppContentFile.</span></span>
## <a name="methods"></a><span data-ttu-id="00683-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="00683-105">Methods</span></span>
|<span data-ttu-id="00683-106">Método</span><span class="sxs-lookup"><span data-stu-id="00683-106">Method</span></span>|<span data-ttu-id="00683-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="00683-107">Return Type</span></span>|<span data-ttu-id="00683-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="00683-108">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="00683-109">Enumerar mobileAppContents</span><span class="sxs-lookup"><span data-stu-id="00683-109">List mobileAppContents</span></span>](../api/intune_apps_mobileappcontent_list.md)|<span data-ttu-id="00683-110">Colección [mobileAppContent](../resources/intune_apps_mobileappcontent.md)</span><span class="sxs-lookup"><span data-stu-id="00683-110">[mobileAppContent](../resources/intune_apps_mobileappcontent.md) collection</span></span>|<span data-ttu-id="00683-111">Enumere las propiedades y las relaciones de los objetos [mobileAppContent](../resources/intune_apps_mobileappcontent.md).</span><span class="sxs-lookup"><span data-stu-id="00683-111">List properties and relationships of the [mobileAppContent](../resources/intune_apps_mobileappcontent.md) objects.</span></span>|
|[<span data-ttu-id="00683-112">Obtener mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="00683-112">Get mobileAppContent</span></span>](../api/intune_apps_mobileappcontent_get.md)|[<span data-ttu-id="00683-113">mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="00683-113">mobileAppContent</span></span>](../resources/intune_apps_mobileappcontent.md)|<span data-ttu-id="00683-114">Lea las propiedades y las relaciones del objeto [mobileAppContent](../resources/intune_apps_mobileappcontent.md).</span><span class="sxs-lookup"><span data-stu-id="00683-114">Read properties and relationships of the [mobileAppContent](../resources/intune_apps_mobileappcontent.md) object.</span></span>|
|[<span data-ttu-id="00683-115">Crear mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="00683-115">Create mobileAppContent</span></span>](../api/intune_apps_mobileappcontent_create.md)|[<span data-ttu-id="00683-116">mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="00683-116">mobileAppContent</span></span>](../resources/intune_apps_mobileappcontent.md)|<span data-ttu-id="00683-117">Cree un objeto [mobileAppContent](../resources/intune_apps_mobileappcontent.md).</span><span class="sxs-lookup"><span data-stu-id="00683-117">Create a new [mobileAppContent](../resources/intune_apps_mobileappcontent.md) object.</span></span>|
|[<span data-ttu-id="00683-118">Eliminar mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="00683-118">Delete mobileAppContent</span></span>](../api/intune_apps_mobileappcontent_delete.md)|<span data-ttu-id="00683-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="00683-119">None</span></span>|<span data-ttu-id="00683-120">Elimina un [mobileAppContent](../resources/intune_apps_mobileappcontent.md)</span><span class="sxs-lookup"><span data-stu-id="00683-120">Deletes a [mobileAppContent](../resources/intune_apps_mobileappcontent.md).</span></span>|
|[<span data-ttu-id="00683-121">Actualizar mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="00683-121">Update mobileAppContent</span></span>](../api/intune_apps_mobileappcontent_update.md)|[<span data-ttu-id="00683-122">mobileAppContent</span><span class="sxs-lookup"><span data-stu-id="00683-122">mobileAppContent</span></span>](../resources/intune_apps_mobileappcontent.md)|<span data-ttu-id="00683-123">Actualice las propiedades de un objeto [mobileAppContent](../resources/intune_apps_mobileappcontent.md).</span><span class="sxs-lookup"><span data-stu-id="00683-123">Update the properties of a [mobileAppContent](../resources/intune_apps_mobileappcontent.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="00683-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="00683-124">Properties</span></span>
|<span data-ttu-id="00683-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="00683-125">Property</span></span>|<span data-ttu-id="00683-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="00683-126">Type</span></span>|<span data-ttu-id="00683-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="00683-127">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="00683-128">id</span><span class="sxs-lookup"><span data-stu-id="00683-128">id</span></span>|<span data-ttu-id="00683-129">String</span><span class="sxs-lookup"><span data-stu-id="00683-129">String</span></span>|<span data-ttu-id="00683-130">La versión de contenido de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="00683-130">The app content version.</span></span>|

## <a name="relationships"></a><span data-ttu-id="00683-131">Relaciones</span><span class="sxs-lookup"><span data-stu-id="00683-131">Relationships</span></span>
|<span data-ttu-id="00683-132">Relación</span><span class="sxs-lookup"><span data-stu-id="00683-132">Relationship</span></span>|<span data-ttu-id="00683-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="00683-133">Type</span></span>|<span data-ttu-id="00683-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="00683-134">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="00683-135">archivos</span><span class="sxs-lookup"><span data-stu-id="00683-135">files</span></span>|<span data-ttu-id="00683-136">Colección [mobileAppContentFile](../resources/intune_apps_mobileappcontentfile.md)</span><span class="sxs-lookup"><span data-stu-id="00683-136">[mobileAppContentFile](../resources/intune_apps_mobileappcontentfile.md) collection</span></span>|<span data-ttu-id="00683-137">La lista de archivos de esta versión de contenido de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="00683-137">The list of files for this app content version.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="00683-138">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="00683-138">JSON Representation</span></span>
<span data-ttu-id="00683-139">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="00683-139">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.mobileAppContent"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileAppContent",
  "id": "String (identifier)"
}
```



