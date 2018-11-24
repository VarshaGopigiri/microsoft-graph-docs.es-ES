# <a name="devicecomplianceuseroverview-resource-type"></a><span data-ttu-id="0a65c-101">Tipo de recurso deviceComplianceUserOverview</span><span class="sxs-lookup"><span data-stu-id="0a65c-101">deviceComplianceUserOverview resource type</span></span>

> <span data-ttu-id="0a65c-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0a65c-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0a65c-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="0a65c-103">Not yet documented</span></span>
## <a name="methods"></a><span data-ttu-id="0a65c-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="0a65c-104">Methods</span></span>
|<span data-ttu-id="0a65c-105">Método</span><span class="sxs-lookup"><span data-stu-id="0a65c-105">Method</span></span>|<span data-ttu-id="0a65c-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0a65c-106">Return Type</span></span>|<span data-ttu-id="0a65c-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="0a65c-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="0a65c-108">Obtener deviceComplianceUserOverview</span><span class="sxs-lookup"><span data-stu-id="0a65c-108">Get deviceComplianceUserOverview</span></span>](../api/intune_deviceconfig_devicecomplianceuseroverview_get.md)|[<span data-ttu-id="0a65c-109">deviceComplianceUserOverview</span><span class="sxs-lookup"><span data-stu-id="0a65c-109">deviceComplianceUserOverview</span></span>](../resources/intune_deviceconfig_devicecomplianceuseroverview.md)|<span data-ttu-id="0a65c-110">Lea las propiedades y las relaciones del objeto [deviceComplianceUserOverview](../resources/intune_deviceconfig_devicecomplianceuseroverview.md).</span><span class="sxs-lookup"><span data-stu-id="0a65c-110">Read properties and relationships of the [deviceComplianceUserOverview](../resources/intune_deviceconfig_devicecomplianceuseroverview.md) object.</span></span>|
|[<span data-ttu-id="0a65c-111">Actualizar deviceComplianceUserOverview</span><span class="sxs-lookup"><span data-stu-id="0a65c-111">Update deviceComplianceUserOverview</span></span>](../api/intune_deviceconfig_devicecomplianceuseroverview_update.md)|[<span data-ttu-id="0a65c-112">deviceComplianceUserOverview</span><span class="sxs-lookup"><span data-stu-id="0a65c-112">deviceComplianceUserOverview</span></span>](../resources/intune_deviceconfig_devicecomplianceuseroverview.md)|<span data-ttu-id="0a65c-113">Actualice las propiedades de un objeto [deviceComplianceUserOverview](../resources/intune_deviceconfig_devicecomplianceuseroverview.md).</span><span class="sxs-lookup"><span data-stu-id="0a65c-113">Update the properties of a [deviceComplianceUserOverview](../resources/intune_deviceconfig_devicecomplianceuseroverview.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="0a65c-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0a65c-114">Properties</span></span>
|<span data-ttu-id="0a65c-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0a65c-115">Property</span></span>|<span data-ttu-id="0a65c-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="0a65c-116">Type</span></span>|<span data-ttu-id="0a65c-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="0a65c-117">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0a65c-118">id</span><span class="sxs-lookup"><span data-stu-id="0a65c-118">id</span></span>|<span data-ttu-id="0a65c-119">cadena</span><span class="sxs-lookup"><span data-stu-id="0a65c-119">String</span></span>|<span data-ttu-id="0a65c-120">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="0a65c-120">Key of the entity.</span></span>|
|<span data-ttu-id="0a65c-121">pendingCount</span><span class="sxs-lookup"><span data-stu-id="0a65c-121">pendingCount</span></span>|<span data-ttu-id="0a65c-122">Int32</span><span class="sxs-lookup"><span data-stu-id="0a65c-122">Int32</span></span>|<span data-ttu-id="0a65c-123">Número de usuarios pendientes</span><span class="sxs-lookup"><span data-stu-id="0a65c-123">Number of pending Users</span></span>|
|<span data-ttu-id="0a65c-124">notApplicableCount</span><span class="sxs-lookup"><span data-stu-id="0a65c-124">notApplicableCount</span></span>|<span data-ttu-id="0a65c-125">Int32</span><span class="sxs-lookup"><span data-stu-id="0a65c-125">Int32</span></span>|<span data-ttu-id="0a65c-126">Número de usuarios no es aplicable.</span><span class="sxs-lookup"><span data-stu-id="0a65c-126">Number of not applicable users</span></span>|
|<span data-ttu-id="0a65c-127">successCount</span><span class="sxs-lookup"><span data-stu-id="0a65c-127">successCount</span></span>|<span data-ttu-id="0a65c-128">Int32</span><span class="sxs-lookup"><span data-stu-id="0a65c-128">Int32</span></span>|<span data-ttu-id="0a65c-129">Número de usuarios correctos</span><span class="sxs-lookup"><span data-stu-id="0a65c-129">Number of succeeded Users</span></span>|
|<span data-ttu-id="0a65c-130">errorCount</span><span class="sxs-lookup"><span data-stu-id="0a65c-130">errorCount</span></span>|<span data-ttu-id="0a65c-131">Int32</span><span class="sxs-lookup"><span data-stu-id="0a65c-131">Int32</span></span>|<span data-ttu-id="0a65c-132">Número de usuarios con error</span><span class="sxs-lookup"><span data-stu-id="0a65c-132">Number of error Users</span></span>|
|<span data-ttu-id="0a65c-133">failedCount</span><span class="sxs-lookup"><span data-stu-id="0a65c-133">failedCount</span></span>|<span data-ttu-id="0a65c-134">Int32</span><span class="sxs-lookup"><span data-stu-id="0a65c-134">Int32</span></span>|<span data-ttu-id="0a65c-135">Número de usuarios erróneos</span><span class="sxs-lookup"><span data-stu-id="0a65c-135">Number of failed Users</span></span>|
|<span data-ttu-id="0a65c-136">lastUpdateDateTime</span><span class="sxs-lookup"><span data-stu-id="0a65c-136">lastUpdateDateTime</span></span>|<span data-ttu-id="0a65c-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0a65c-137">DateTimeOffset</span></span>|<span data-ttu-id="0a65c-138">Última hora de actualización</span><span class="sxs-lookup"><span data-stu-id="0a65c-138">Last update time</span></span>|
|<span data-ttu-id="0a65c-139">configurationVersion</span><span class="sxs-lookup"><span data-stu-id="0a65c-139">configurationVersion</span></span>|<span data-ttu-id="0a65c-140">Int32</span><span class="sxs-lookup"><span data-stu-id="0a65c-140">Int32</span></span>|<span data-ttu-id="0a65c-141">Versión de la directiva para esa información general</span><span class="sxs-lookup"><span data-stu-id="0a65c-141">Version of the policy for that overview</span></span>|

## <a name="relationships"></a><span data-ttu-id="0a65c-142">Relaciones</span><span class="sxs-lookup"><span data-stu-id="0a65c-142">Relationships</span></span>
<span data-ttu-id="0a65c-143">Ninguna</span><span class="sxs-lookup"><span data-stu-id="0a65c-143">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="0a65c-144">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0a65c-144">JSON Representation</span></span>
<span data-ttu-id="0a65c-145">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="0a65c-145">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceComplianceUserOverview"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceComplianceUserOverview",
  "id": "String (identifier)",
  "pendingCount": 1024,
  "notApplicableCount": 1024,
  "successCount": 1024,
  "errorCount": 1024,
  "failedCount": 1024,
  "lastUpdateDateTime": "String (timestamp)",
  "configurationVersion": 1024
}
```



