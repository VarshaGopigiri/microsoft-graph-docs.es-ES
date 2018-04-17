# <a name="devicemanagement-resource-type"></a><span data-ttu-id="ed892-101">Tipo de recurso deviceManagement</span><span class="sxs-lookup"><span data-stu-id="ed892-101">deviceManagement resource type</span></span>

> <span data-ttu-id="ed892-102">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ed892-102">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ed892-103">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ed892-103">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ed892-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ed892-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ed892-105">Entidad singleton que actúa como un contenedor para todas las funcionalidades de administración de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="ed892-105">Singleton entity that acts as a container for all device management functionality.</span></span>
## <a name="methods"></a><span data-ttu-id="ed892-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="ed892-106">Methods</span></span>
|<span data-ttu-id="ed892-107">Método</span><span class="sxs-lookup"><span data-stu-id="ed892-107">Method</span></span>|<span data-ttu-id="ed892-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ed892-108">Return Type</span></span>|<span data-ttu-id="ed892-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed892-109">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="ed892-110">Obtener deviceManagement</span><span class="sxs-lookup"><span data-stu-id="ed892-110">Get deviceManagement</span></span>](../api/intune_troubleshooting_devicemanagement_get.md)|[<span data-ttu-id="ed892-111">deviceManagement</span><span class="sxs-lookup"><span data-stu-id="ed892-111">deviceManagement</span></span>](../resources/intune_troubleshooting_devicemanagement.md)|<span data-ttu-id="ed892-112">Lea las propiedades y las relaciones del objeto [deviceManagement](../resources/intune_troubleshooting_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="ed892-112">Read properties and relationships of the [deviceManagement](../resources/intune_troubleshooting_devicemanagement.md) object.</span></span>|
|[<span data-ttu-id="ed892-113">Actualizar deviceManagement</span><span class="sxs-lookup"><span data-stu-id="ed892-113">Update deviceManagement</span></span>](../api/intune_troubleshooting_devicemanagement_update.md)|[<span data-ttu-id="ed892-114">deviceManagement</span><span class="sxs-lookup"><span data-stu-id="ed892-114">deviceManagement</span></span>](../resources/intune_troubleshooting_devicemanagement.md)|<span data-ttu-id="ed892-115">Actualice las propiedades de un objeto [deviceManagement](../resources/intune_troubleshooting_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="ed892-115">Update the properties of a [deviceManagement](../resources/intune_troubleshooting_devicemanagement.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="ed892-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ed892-116">Properties</span></span>
|<span data-ttu-id="ed892-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ed892-117">Property</span></span>|<span data-ttu-id="ed892-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed892-118">Type</span></span>|<span data-ttu-id="ed892-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed892-119">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ed892-120">id</span><span class="sxs-lookup"><span data-stu-id="ed892-120">id</span></span>|<span data-ttu-id="ed892-121">String</span><span class="sxs-lookup"><span data-stu-id="ed892-121">String</span></span>|<span data-ttu-id="ed892-122">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="ed892-122">Not yet documented</span></span>|

## <a name="relationships"></a><span data-ttu-id="ed892-123">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ed892-123">Relationships</span></span>
|<span data-ttu-id="ed892-124">Relación</span><span class="sxs-lookup"><span data-stu-id="ed892-124">Relationship</span></span>|<span data-ttu-id="ed892-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed892-125">Type</span></span>|<span data-ttu-id="ed892-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed892-126">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ed892-127">troubleshootingEvents</span><span class="sxs-lookup"><span data-stu-id="ed892-127">troubleshootingEvents</span></span>|<span data-ttu-id="ed892-128">Colección [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span><span class="sxs-lookup"><span data-stu-id="ed892-128">[deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md) collection</span></span>|<span data-ttu-id="ed892-129">La lista de eventos de solución de problemas del espacio empresarial.</span><span class="sxs-lookup"><span data-stu-id="ed892-129">The list of troubleshooting events for the tenant.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="ed892-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ed892-130">JSON Representation</span></span>
<span data-ttu-id="ed892-131">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ed892-131">Here is a JSON representation of the resource.</span></span>
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



