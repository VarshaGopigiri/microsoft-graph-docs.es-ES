# <a name="devicemanagement-resource-type"></a><span data-ttu-id="84523-101">Tipo de recurso deviceManagement</span><span class="sxs-lookup"><span data-stu-id="84523-101">deviceManagement resource type</span></span>

> <span data-ttu-id="84523-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="84523-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="84523-103">Entidad singleton que actúa como un contenedor para todas las funcionalidades de administración de aplicaciones de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="84523-103">Singleton entity that acts as a container for all device app management functionality.</span></span>
## <a name="methods"></a><span data-ttu-id="84523-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="84523-104">Methods</span></span>
|<span data-ttu-id="84523-105">Método</span><span class="sxs-lookup"><span data-stu-id="84523-105">Method</span></span>|<span data-ttu-id="84523-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="84523-106">Return Type</span></span>|<span data-ttu-id="84523-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="84523-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="84523-108">Obtener deviceManagement</span><span class="sxs-lookup"><span data-stu-id="84523-108">Get deviceManagement</span></span>](../api/intune_auditing_devicemanagement_get.md)|[<span data-ttu-id="84523-109">deviceManagement</span><span class="sxs-lookup"><span data-stu-id="84523-109">deviceManagement</span></span>](../resources/intune_auditing_devicemanagement.md)|<span data-ttu-id="84523-110">Lea las propiedades y las relaciones del objeto [deviceManagement](../resources/intune_auditing_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="84523-110">Read properties and relationships of [plannerTaskDetails](../resources/intune_auditing_devicemanagement.md) object.</span></span>|
|[<span data-ttu-id="84523-111">Actualizar deviceManagement</span><span class="sxs-lookup"><span data-stu-id="84523-111">Update deviceManagement</span></span>](../api/intune_auditing_devicemanagement_update.md)|[<span data-ttu-id="84523-112">deviceManagement</span><span class="sxs-lookup"><span data-stu-id="84523-112">deviceManagement</span></span>](../resources/intune_auditing_devicemanagement.md)|<span data-ttu-id="84523-113">Actualice las propiedades de un objeto [deviceManagement](../resources/intune_auditing_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="84523-113">Update the properties of a [calendar](../resources/intune_auditing_devicemanagement.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="84523-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="84523-114">Properties</span></span>
|<span data-ttu-id="84523-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="84523-115">Property</span></span>|<span data-ttu-id="84523-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="84523-116">Type</span></span>|<span data-ttu-id="84523-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="84523-117">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="84523-118">id</span><span class="sxs-lookup"><span data-stu-id="84523-118">id</span></span>|<span data-ttu-id="84523-119">cadena</span><span class="sxs-lookup"><span data-stu-id="84523-119">String</span></span>|<span data-ttu-id="84523-120">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="84523-120">Key of the setting.</span></span>|

## <a name="relationships"></a><span data-ttu-id="84523-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="84523-121">Relationships</span></span>
|<span data-ttu-id="84523-122">Relación</span><span class="sxs-lookup"><span data-stu-id="84523-122">Relationship</span></span>|<span data-ttu-id="84523-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="84523-123">Type</span></span>|<span data-ttu-id="84523-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="84523-124">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="84523-125">auditEvents</span><span class="sxs-lookup"><span data-stu-id="84523-125">auditEvents</span></span>|<span data-ttu-id="84523-126">Colección [auditEvent](../resources/intune_auditing_auditevent.md)</span><span class="sxs-lookup"><span data-stu-id="84523-126">[auditEvent](../resources/intune_auditing_auditevent.md) collection</span></span>|<span data-ttu-id="84523-127">Los eventos de auditoría</span><span class="sxs-lookup"><span data-stu-id="84523-127">The Audit Events</span></span>|

## <a name="json-representation"></a><span data-ttu-id="84523-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="84523-128">JSON Representation</span></span>
<span data-ttu-id="84523-129">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="84523-129">Here is a JSON representation of the resource.</span></span>
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



