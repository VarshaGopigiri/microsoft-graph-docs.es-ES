# <a name="devicemanagement-resource-type"></a><span data-ttu-id="1076d-101">Tipo de recurso deviceManagement</span><span class="sxs-lookup"><span data-stu-id="1076d-101">deviceManagement resource type</span></span>

> <span data-ttu-id="1076d-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1076d-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1076d-103">Entidad singleton que actúa como un contenedor para todas las funcionalidades de administración de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="1076d-103">Singleton entity that acts as a container for all device management functionality.</span></span>
## <a name="methods"></a><span data-ttu-id="1076d-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="1076d-104">Methods</span></span>
|<span data-ttu-id="1076d-105">Método</span><span class="sxs-lookup"><span data-stu-id="1076d-105">Method</span></span>|<span data-ttu-id="1076d-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1076d-106">Return Type</span></span>|<span data-ttu-id="1076d-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="1076d-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="1076d-108">Obtener deviceManagement</span><span class="sxs-lookup"><span data-stu-id="1076d-108">Get deviceManagement</span></span>](../api/intune_notification_devicemanagement_get.md)|[<span data-ttu-id="1076d-109">deviceManagement</span><span class="sxs-lookup"><span data-stu-id="1076d-109">deviceManagement</span></span>](../resources/intune_notification_devicemanagement.md)|<span data-ttu-id="1076d-110">Lea las propiedades y las relaciones del objeto [deviceManagement](../resources/intune_notification_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="1076d-110">Read properties and relationships of [plannerTaskDetails](../resources/intune_notification_devicemanagement.md) object.</span></span>|
|[<span data-ttu-id="1076d-111">Actualizar deviceManagement</span><span class="sxs-lookup"><span data-stu-id="1076d-111">Update deviceManagement</span></span>](../api/intune_notification_devicemanagement_update.md)|[<span data-ttu-id="1076d-112">deviceManagement</span><span class="sxs-lookup"><span data-stu-id="1076d-112">deviceManagement</span></span>](../resources/intune_notification_devicemanagement.md)|<span data-ttu-id="1076d-113">Actualice las propiedades de un objeto [deviceManagement](../resources/intune_notification_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="1076d-113">Update the properties of a [calendar](../resources/intune_notification_devicemanagement.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="1076d-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1076d-114">Properties</span></span>
|<span data-ttu-id="1076d-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1076d-115">Property</span></span>|<span data-ttu-id="1076d-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="1076d-116">Type</span></span>|<span data-ttu-id="1076d-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="1076d-117">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1076d-118">id</span><span class="sxs-lookup"><span data-stu-id="1076d-118">id</span></span>|<span data-ttu-id="1076d-119">cadena</span><span class="sxs-lookup"><span data-stu-id="1076d-119">String</span></span>|<span data-ttu-id="1076d-120">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="1076d-120">Not yet documented</span></span>|

## <a name="relationships"></a><span data-ttu-id="1076d-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="1076d-121">Relationships</span></span>
|<span data-ttu-id="1076d-122">Relación</span><span class="sxs-lookup"><span data-stu-id="1076d-122">Relationship</span></span>|<span data-ttu-id="1076d-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="1076d-123">Type</span></span>|<span data-ttu-id="1076d-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="1076d-124">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1076d-125">notificationMessageTemplates</span><span class="sxs-lookup"><span data-stu-id="1076d-125">notificationMessageTemplates</span></span>|<span data-ttu-id="1076d-126">Colección [notificationMessageTemplate](../resources/intune_notification_notificationmessagetemplate.md)</span><span class="sxs-lookup"><span data-stu-id="1076d-126">[notificationMessageTemplate](../resources/intune_notification_notificationmessagetemplate.md) collection</span></span>|<span data-ttu-id="1076d-127">Las plantillas de mensajes de notificación.</span><span class="sxs-lookup"><span data-stu-id="1076d-127">The Notification Message Templates.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="1076d-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1076d-128">JSON Representation</span></span>
<span data-ttu-id="1076d-129">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="1076d-129">Here is a JSON representation of the resource.</span></span>
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



