# <a name="devicemanagement-resource-type"></a><span data-ttu-id="ed0e0-101">Tipo de recurso deviceManagement</span><span class="sxs-lookup"><span data-stu-id="ed0e0-101">deviceManagement resource type</span></span>

> <span data-ttu-id="ed0e0-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ed0e0-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ed0e0-103">Entidad singleton que actúa como un contenedor para todas las funcionalidades de administración de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="ed0e0-103">Singleton entity that acts as a container for all device management functionality.</span></span>
## <a name="methods"></a><span data-ttu-id="ed0e0-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="ed0e0-104">Methods</span></span>
|<span data-ttu-id="ed0e0-105">Método</span><span class="sxs-lookup"><span data-stu-id="ed0e0-105">Method</span></span>|<span data-ttu-id="ed0e0-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ed0e0-106">Return Type</span></span>|<span data-ttu-id="ed0e0-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed0e0-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="ed0e0-108">Obtener deviceManagement</span><span class="sxs-lookup"><span data-stu-id="ed0e0-108">Get deviceManagement</span></span>](../api/intune_remoteassistance_devicemanagement_get.md)|[<span data-ttu-id="ed0e0-109">deviceManagement</span><span class="sxs-lookup"><span data-stu-id="ed0e0-109">deviceManagement</span></span>](../resources/intune_remoteassistance_devicemanagement.md)|<span data-ttu-id="ed0e0-110">Lea las propiedades y las relaciones del objeto [deviceManagement](../resources/intune_remoteassistance_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="ed0e0-110">Read properties and relationships of [plannerTaskDetails](../resources/intune_remoteassistance_devicemanagement.md) object.</span></span>|
|[<span data-ttu-id="ed0e0-111">Actualizar deviceManagement</span><span class="sxs-lookup"><span data-stu-id="ed0e0-111">Update deviceManagement</span></span>](../api/intune_remoteassistance_devicemanagement_update.md)|[<span data-ttu-id="ed0e0-112">deviceManagement</span><span class="sxs-lookup"><span data-stu-id="ed0e0-112">deviceManagement</span></span>](../resources/intune_remoteassistance_devicemanagement.md)|<span data-ttu-id="ed0e0-113">Actualice las propiedades de un objeto [deviceManagement](../resources/intune_remoteassistance_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="ed0e0-113">Update the properties of a [calendar](../resources/intune_remoteassistance_devicemanagement.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="ed0e0-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ed0e0-114">Properties</span></span>
|<span data-ttu-id="ed0e0-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ed0e0-115">Property</span></span>|<span data-ttu-id="ed0e0-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed0e0-116">Type</span></span>|<span data-ttu-id="ed0e0-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed0e0-117">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ed0e0-118">id</span><span class="sxs-lookup"><span data-stu-id="ed0e0-118">id</span></span>|<span data-ttu-id="ed0e0-119">cadena</span><span class="sxs-lookup"><span data-stu-id="ed0e0-119">String</span></span>|<span data-ttu-id="ed0e0-120">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="ed0e0-120">Not yet documented</span></span>|

## <a name="relationships"></a><span data-ttu-id="ed0e0-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ed0e0-121">Relationships</span></span>
|<span data-ttu-id="ed0e0-122">Relación</span><span class="sxs-lookup"><span data-stu-id="ed0e0-122">Relationship</span></span>|<span data-ttu-id="ed0e0-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed0e0-123">Type</span></span>|<span data-ttu-id="ed0e0-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed0e0-124">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ed0e0-125">remoteAssistancePartners</span><span class="sxs-lookup"><span data-stu-id="ed0e0-125">remoteAssistancePartners</span></span>|<span data-ttu-id="ed0e0-126">Colección [remoteAssistancePartner](../resources/intune_remoteassistance_remoteassistancepartner.md)</span><span class="sxs-lookup"><span data-stu-id="ed0e0-126">[remoteAssistancePartner](../resources/intune_remoteassistance_remoteassistancepartner.md) collection</span></span>|<span data-ttu-id="ed0e0-127">Los partners de asistencia remota.</span><span class="sxs-lookup"><span data-stu-id="ed0e0-127">The remote assist partners.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="ed0e0-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ed0e0-128">JSON Representation</span></span>
<span data-ttu-id="ed0e0-129">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ed0e0-129">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceManagement"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagement",
  "id": "String (identifier)"
}
```



