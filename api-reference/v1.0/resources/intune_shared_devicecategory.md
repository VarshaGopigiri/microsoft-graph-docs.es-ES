# <a name="devicecategory-resource-type"></a><span data-ttu-id="01c51-101">Tipo de recurso deviceCategory</span><span class="sxs-lookup"><span data-stu-id="01c51-101">deviceCategory resource type</span></span>

> <span data-ttu-id="01c51-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="01c51-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="01c51-103">Las categorías de dispositivo proporcionan una forma de organizar sus dispositivos.</span><span class="sxs-lookup"><span data-stu-id="01c51-103">Device categories provides a way to organize your devices.</span></span> <span data-ttu-id="01c51-104">Al usar categorías de dispositivos, los administradores de la compañía pueden definir las categorías de forma pertinente para su empresa.</span><span class="sxs-lookup"><span data-stu-id="01c51-104">Using device categories, company administrators can define their own categories that make sense to their company.</span></span> <span data-ttu-id="01c51-105">A continuación, estas categorías se pueden aplicar a un dispositivo en la consola de Azure de Intune o un usuario puede seleccionarlas durante la inscripción de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="01c51-105">These categories can then be applied to a device in the Intune Azure console or selected by a user during device enrollment.</span></span> <span data-ttu-id="01c51-106">Puede filtrar los informes y crear grupos de dispositivos de Azure Active Directory dinámicos según las categorías de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="01c51-106">You can filter reports and create dynamic Azure Active Directory device groups based on device categories.</span></span>

## <a name="methods"></a><span data-ttu-id="01c51-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="01c51-107">Methods</span></span>
|<span data-ttu-id="01c51-108">Método</span><span class="sxs-lookup"><span data-stu-id="01c51-108">Method</span></span>|<span data-ttu-id="01c51-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="01c51-109">Return Type</span></span>|<span data-ttu-id="01c51-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="01c51-110">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="01c51-111">Objetos [Listar deviceCategories](../api/intune_shared_devicecategory_list.md).</span><span class="sxs-lookup"><span data-stu-id="01c51-111">[List deviceCategories](../api/intune_shared_devicecategory_list.md) objects.</span></span>|
|<span data-ttu-id="01c51-112">Objeto [Obtener deviceCategory](../api/intune_shared_devicecategory_get.md).</span><span class="sxs-lookup"><span data-stu-id="01c51-112">[Get deviceCategory](../api/intune_shared_devicecategory_get.md) object.</span></span>|
|<span data-ttu-id="01c51-113">Objeto [Crear deviceCategory](../api/intune_shared_devicecategory_create.md).</span><span class="sxs-lookup"><span data-stu-id="01c51-113">Create a new [deviceCategory](../api/intune_shared_devicecategory_create.md) object.</span></span>|
|<span data-ttu-id="01c51-114">[Eliminar deviceCategory](../api/intune_shared_devicecategory_delete.md).</span><span class="sxs-lookup"><span data-stu-id="01c51-114">Delete deviceCategory</span></span>|
|<span data-ttu-id="01c51-115">Objeto [Actualizar deviceCategory](../api/intune_shared_devicecategory_update.md).</span><span class="sxs-lookup"><span data-stu-id="01c51-115">Update the properties of a [deviceCategory](../api/intune_shared_devicecategory_update.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="01c51-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="01c51-116">Properties</span></span>
|<span data-ttu-id="01c51-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="01c51-117">Property</span></span>|<span data-ttu-id="01c51-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="01c51-118">Type</span></span>|<span data-ttu-id="01c51-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="01c51-119">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="01c51-120">id</span><span class="sxs-lookup"><span data-stu-id="01c51-120">id</span></span>|<span data-ttu-id="01c51-121">Cadena</span><span class="sxs-lookup"><span data-stu-id="01c51-121">String</span></span>|<span data-ttu-id="01c51-122">El identificador único de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="01c51-122">Unique identifier for the device category.</span></span> <span data-ttu-id="01c51-123">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="01c51-123">Read-only.</span></span>|
|<span data-ttu-id="01c51-124">**Incorporación**</span><span class="sxs-lookup"><span data-stu-id="01c51-124">**On-boarding**</span></span>|
|<span data-ttu-id="01c51-125">displayName</span><span class="sxs-lookup"><span data-stu-id="01c51-125">displayName</span></span>|<span data-ttu-id="01c51-126">Cadena</span><span class="sxs-lookup"><span data-stu-id="01c51-126">String</span></span>|<span data-ttu-id="01c51-127">Nombre para mostrar de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="01c51-127">Display name for the device category.</span></span>|
|<span data-ttu-id="01c51-128">descripción</span><span class="sxs-lookup"><span data-stu-id="01c51-128">description</span></span>|<span data-ttu-id="01c51-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="01c51-129">String</span></span>|<span data-ttu-id="01c51-130">Descripción opcional de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="01c51-130">Optional description for the device category.</span></span>|

## <a name="relationships"></a><span data-ttu-id="01c51-131">Relaciones</span><span class="sxs-lookup"><span data-stu-id="01c51-131">Relationships</span></span>
<span data-ttu-id="01c51-132">Ninguna</span><span class="sxs-lookup"><span data-stu-id="01c51-132">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="01c51-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="01c51-133">JSON Representation</span></span>
<span data-ttu-id="01c51-134">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="01c51-134">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.deviceCategory"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceCategory",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String"
}
```



