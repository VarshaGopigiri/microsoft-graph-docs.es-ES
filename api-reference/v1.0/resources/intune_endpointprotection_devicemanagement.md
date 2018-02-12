# <a name="devicemanagement-resource-type"></a><span data-ttu-id="d020b-101">Tipo de recurso deviceManagement</span><span class="sxs-lookup"><span data-stu-id="d020b-101">deviceManagement resource type</span></span>

> <span data-ttu-id="d020b-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d020b-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d020b-103">Entidad singleton que actúa como un contenedor para todas las funcionalidades de administración de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="d020b-103">Singleton entity that acts as a container for all device management functionality.</span></span>
## <a name="methods"></a><span data-ttu-id="d020b-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="d020b-104">Methods</span></span>
|<span data-ttu-id="d020b-105">Método</span><span class="sxs-lookup"><span data-stu-id="d020b-105">Method</span></span>|<span data-ttu-id="d020b-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d020b-106">Return Type</span></span>|<span data-ttu-id="d020b-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="d020b-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="d020b-108">Obtener deviceManagement</span><span class="sxs-lookup"><span data-stu-id="d020b-108">Get deviceManagement</span></span>](../api/intune_endpointprotection_devicemanagement_get.md)|[<span data-ttu-id="d020b-109">deviceManagement</span><span class="sxs-lookup"><span data-stu-id="d020b-109">deviceManagement</span></span>](../resources/intune_endpointprotection_devicemanagement.md)|<span data-ttu-id="d020b-110">Lea las propiedades y las relaciones del objeto [deviceManagement](../resources/intune_endpointprotection_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="d020b-110">Read properties and relationships of [plannerTaskDetails](../resources/intune_endpointprotection_devicemanagement.md) object.</span></span>|
|[<span data-ttu-id="d020b-111">Actualizar deviceManagement</span><span class="sxs-lookup"><span data-stu-id="d020b-111">Update deviceManagement</span></span>](../api/intune_endpointprotection_devicemanagement_update.md)|[<span data-ttu-id="d020b-112">deviceManagement</span><span class="sxs-lookup"><span data-stu-id="d020b-112">deviceManagement</span></span>](../resources/intune_endpointprotection_devicemanagement.md)|<span data-ttu-id="d020b-113">Actualice las propiedades de un objeto [deviceManagement](../resources/intune_endpointprotection_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="d020b-113">Update the properties of a [calendar](../resources/intune_endpointprotection_devicemanagement.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="d020b-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d020b-114">Properties</span></span>
|<span data-ttu-id="d020b-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d020b-115">Property</span></span>|<span data-ttu-id="d020b-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="d020b-116">Type</span></span>|<span data-ttu-id="d020b-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="d020b-117">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d020b-118">id</span><span class="sxs-lookup"><span data-stu-id="d020b-118">id</span></span>|<span data-ttu-id="d020b-119">cadena</span><span class="sxs-lookup"><span data-stu-id="d020b-119">String</span></span>|<span data-ttu-id="d020b-120">Identificador único</span><span class="sxs-lookup"><span data-stu-id="d020b-120">Unique Identifier</span></span>|

## <a name="relationships"></a><span data-ttu-id="d020b-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d020b-121">Relationships</span></span>
<span data-ttu-id="d020b-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="d020b-122">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="d020b-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d020b-123">JSON Representation</span></span>
<span data-ttu-id="d020b-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d020b-124">Here is a JSON representation of the resource.</span></span>
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



