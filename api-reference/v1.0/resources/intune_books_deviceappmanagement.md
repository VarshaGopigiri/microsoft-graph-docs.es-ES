# <a name="deviceappmanagement-resource-type"></a><span data-ttu-id="a9ab5-101">Tipo de recurso deviceAppManagement</span><span class="sxs-lookup"><span data-stu-id="a9ab5-101">deviceAppManagement resource type</span></span>

> <span data-ttu-id="a9ab5-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a9ab5-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a9ab5-103">Entidad singleton que actúa como un contenedor para todas las funcionalidades de administración de aplicaciones de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a9ab5-103">Singleton entity that acts as a container for all device app management functionality.</span></span>
## <a name="methods"></a><span data-ttu-id="a9ab5-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="a9ab5-104">Methods</span></span>
|<span data-ttu-id="a9ab5-105">Método</span><span class="sxs-lookup"><span data-stu-id="a9ab5-105">Method</span></span>|<span data-ttu-id="a9ab5-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a9ab5-106">Return Type</span></span>|<span data-ttu-id="a9ab5-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="a9ab5-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="a9ab5-108">Obtener deviceAppManagement</span><span class="sxs-lookup"><span data-stu-id="a9ab5-108">Get deviceAppManagement</span></span>](../api/intune_books_deviceappmanagement_get.md)|[<span data-ttu-id="a9ab5-109">deviceAppManagement</span><span class="sxs-lookup"><span data-stu-id="a9ab5-109">deviceAppManagement</span></span>](../resources/intune_books_deviceappmanagement.md)|<span data-ttu-id="a9ab5-110">Lea las propiedades y las relaciones del objeto [deviceAppManagement](../resources/intune_books_deviceappmanagement.md).</span><span class="sxs-lookup"><span data-stu-id="a9ab5-110">Read properties and relationships of [plannerTaskDetails](../resources/intune_books_deviceappmanagement.md) object.</span></span>|
|[<span data-ttu-id="a9ab5-111">Actualizar deviceAppManagement</span><span class="sxs-lookup"><span data-stu-id="a9ab5-111">Update deviceAppManagement</span></span>](../api/intune_books_deviceappmanagement_update.md)|[<span data-ttu-id="a9ab5-112">deviceAppManagement</span><span class="sxs-lookup"><span data-stu-id="a9ab5-112">deviceAppManagement</span></span>](../resources/intune_books_deviceappmanagement.md)|<span data-ttu-id="a9ab5-113">Actualice las propiedades de un objeto [deviceAppManagement](../resources/intune_books_deviceappmanagement.md).</span><span class="sxs-lookup"><span data-stu-id="a9ab5-113">Update the properties of a [calendar](../resources/intune_books_deviceappmanagement.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="a9ab5-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a9ab5-114">Properties</span></span>
|<span data-ttu-id="a9ab5-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a9ab5-115">Property</span></span>|<span data-ttu-id="a9ab5-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="a9ab5-116">Type</span></span>|<span data-ttu-id="a9ab5-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="a9ab5-117">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a9ab5-118">id</span><span class="sxs-lookup"><span data-stu-id="a9ab5-118">id</span></span>|<span data-ttu-id="a9ab5-119">cadena</span><span class="sxs-lookup"><span data-stu-id="a9ab5-119">String</span></span>|<span data-ttu-id="a9ab5-120">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="a9ab5-120">Key of the setting.</span></span>|

## <a name="relationships"></a><span data-ttu-id="a9ab5-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a9ab5-121">Relationships</span></span>
|<span data-ttu-id="a9ab5-122">Relación</span><span class="sxs-lookup"><span data-stu-id="a9ab5-122">Relationship</span></span>|<span data-ttu-id="a9ab5-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="a9ab5-123">Type</span></span>|<span data-ttu-id="a9ab5-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="a9ab5-124">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a9ab5-125">managedEBooks</span><span class="sxs-lookup"><span data-stu-id="a9ab5-125">managedEBooks</span></span>|<span data-ttu-id="a9ab5-126">Colección [managedEBook](../resources/intune_books_managedebook.md)</span><span class="sxs-lookup"><span data-stu-id="a9ab5-126">[managedEBook](../resources/intune_books_managedebook.md) collection</span></span>|<span data-ttu-id="a9ab5-127">El libro electrónico Managed.</span><span class="sxs-lookup"><span data-stu-id="a9ab5-127">The Managed eBook.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="a9ab5-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a9ab5-128">JSON Representation</span></span>
<span data-ttu-id="a9ab5-129">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a9ab5-129">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceAppManagement"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceAppManagement",
  "id": "String (identifier)"
}
```



