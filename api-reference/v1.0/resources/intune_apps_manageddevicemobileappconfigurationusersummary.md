# <a name="manageddevicemobileappconfigurationusersummary-resource-type"></a><span data-ttu-id="ba0dd-101">Tipo de recurso managedDeviceMobileAppConfigurationUserSummary</span><span class="sxs-lookup"><span data-stu-id="ba0dd-101">managedDeviceMobileAppConfigurationUserSummary resource type</span></span>

> <span data-ttu-id="ba0dd-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ba0dd-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ba0dd-103">Contiene las propiedades, las propiedades heredadas y las acciones para un resumen de estado de usuario de la configuración de aplicaciones móviles de MDM.</span><span class="sxs-lookup"><span data-stu-id="ba0dd-103">Contains properties, inherited properties and actions for an MDM mobile app configuration user status summary.</span></span>
## <a name="methods"></a><span data-ttu-id="ba0dd-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="ba0dd-104">Methods</span></span>
|<span data-ttu-id="ba0dd-105">Método</span><span class="sxs-lookup"><span data-stu-id="ba0dd-105">Method</span></span>|<span data-ttu-id="ba0dd-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ba0dd-106">Return Type</span></span>|<span data-ttu-id="ba0dd-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="ba0dd-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="ba0dd-108">Obtener managedDeviceMobileAppConfigurationUserSummary</span><span class="sxs-lookup"><span data-stu-id="ba0dd-108">Get managedDeviceMobileAppConfigurationUserSummary</span></span>](../api/intune_apps_manageddevicemobileappconfigurationusersummary_get.md)|[<span data-ttu-id="ba0dd-109">managedDeviceMobileAppConfigurationUserSummary</span><span class="sxs-lookup"><span data-stu-id="ba0dd-109">managedDeviceMobileAppConfigurationUserSummary</span></span>](../resources/intune_apps_manageddevicemobileappconfigurationusersummary.md)|<span data-ttu-id="ba0dd-110">Lea las propiedades y las relaciones del objeto [managedDeviceMobileAppConfigurationUserSummary](../resources/intune_apps_manageddevicemobileappconfigurationusersummary.md).</span><span class="sxs-lookup"><span data-stu-id="ba0dd-110">Read properties and relationships of the [managedDeviceMobileAppConfigurationUserSummary](../resources/intune_apps_manageddevicemobileappconfigurationusersummary.md) object.</span></span>|
|[<span data-ttu-id="ba0dd-111">Actualizar managedDeviceMobileAppConfigurationUserSummary</span><span class="sxs-lookup"><span data-stu-id="ba0dd-111">Update managedDeviceMobileAppConfigurationUserSummary</span></span>](../api/intune_apps_manageddevicemobileappconfigurationusersummary_update.md)|[<span data-ttu-id="ba0dd-112">managedDeviceMobileAppConfigurationUserSummary</span><span class="sxs-lookup"><span data-stu-id="ba0dd-112">managedDeviceMobileAppConfigurationUserSummary</span></span>](../resources/intune_apps_manageddevicemobileappconfigurationusersummary.md)|<span data-ttu-id="ba0dd-113">Actualice las propiedades de un objeto [managedDeviceMobileAppConfigurationUserSummary](../resources/intune_apps_manageddevicemobileappconfigurationusersummary.md).</span><span class="sxs-lookup"><span data-stu-id="ba0dd-113">Update the properties of a [managedDeviceMobileAppConfigurationUserSummary](../resources/intune_apps_manageddevicemobileappconfigurationusersummary.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="ba0dd-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ba0dd-114">Properties</span></span>
|<span data-ttu-id="ba0dd-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ba0dd-115">Property</span></span>|<span data-ttu-id="ba0dd-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="ba0dd-116">Type</span></span>|<span data-ttu-id="ba0dd-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="ba0dd-117">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ba0dd-118">id</span><span class="sxs-lookup"><span data-stu-id="ba0dd-118">id</span></span>|<span data-ttu-id="ba0dd-119">cadena</span><span class="sxs-lookup"><span data-stu-id="ba0dd-119">String</span></span>|<span data-ttu-id="ba0dd-120">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="ba0dd-120">Key of the entity.</span></span>|
|<span data-ttu-id="ba0dd-121">pendingCount</span><span class="sxs-lookup"><span data-stu-id="ba0dd-121">pendingCount</span></span>|<span data-ttu-id="ba0dd-122">Int32</span><span class="sxs-lookup"><span data-stu-id="ba0dd-122">Int32</span></span>|<span data-ttu-id="ba0dd-123">Número de usuarios pendientes</span><span class="sxs-lookup"><span data-stu-id="ba0dd-123">Number of pending Users</span></span>|
|<span data-ttu-id="ba0dd-124">notApplicableCount</span><span class="sxs-lookup"><span data-stu-id="ba0dd-124">notApplicableCount</span></span>|<span data-ttu-id="ba0dd-125">Int32</span><span class="sxs-lookup"><span data-stu-id="ba0dd-125">Int32</span></span>|<span data-ttu-id="ba0dd-126">Número de usuarios no es aplicable.</span><span class="sxs-lookup"><span data-stu-id="ba0dd-126">Number of not applicable users</span></span>|
|<span data-ttu-id="ba0dd-127">successCount</span><span class="sxs-lookup"><span data-stu-id="ba0dd-127">successCount</span></span>|<span data-ttu-id="ba0dd-128">Int32</span><span class="sxs-lookup"><span data-stu-id="ba0dd-128">Int32</span></span>|<span data-ttu-id="ba0dd-129">Número de usuarios correctos</span><span class="sxs-lookup"><span data-stu-id="ba0dd-129">Number of succeeded Users</span></span>|
|<span data-ttu-id="ba0dd-130">errorCount</span><span class="sxs-lookup"><span data-stu-id="ba0dd-130">errorCount</span></span>|<span data-ttu-id="ba0dd-131">Int32</span><span class="sxs-lookup"><span data-stu-id="ba0dd-131">Int32</span></span>|<span data-ttu-id="ba0dd-132">Número de usuarios con error</span><span class="sxs-lookup"><span data-stu-id="ba0dd-132">Number of error Users</span></span>|
|<span data-ttu-id="ba0dd-133">failedCount</span><span class="sxs-lookup"><span data-stu-id="ba0dd-133">failedCount</span></span>|<span data-ttu-id="ba0dd-134">Int32</span><span class="sxs-lookup"><span data-stu-id="ba0dd-134">Int32</span></span>|<span data-ttu-id="ba0dd-135">Número de usuarios erróneos</span><span class="sxs-lookup"><span data-stu-id="ba0dd-135">Number of failed Users</span></span>|
|<span data-ttu-id="ba0dd-136">lastUpdateDateTime</span><span class="sxs-lookup"><span data-stu-id="ba0dd-136">lastUpdateDateTime</span></span>|<span data-ttu-id="ba0dd-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ba0dd-137">DateTimeOffset</span></span>|<span data-ttu-id="ba0dd-138">Última hora de actualización</span><span class="sxs-lookup"><span data-stu-id="ba0dd-138">Last update time</span></span>|
|<span data-ttu-id="ba0dd-139">configurationVersion</span><span class="sxs-lookup"><span data-stu-id="ba0dd-139">configurationVersion</span></span>|<span data-ttu-id="ba0dd-140">Int32</span><span class="sxs-lookup"><span data-stu-id="ba0dd-140">Int32</span></span>|<span data-ttu-id="ba0dd-141">Versión de la directiva para esa información general</span><span class="sxs-lookup"><span data-stu-id="ba0dd-141">Version of the policy for that overview</span></span>|

## <a name="relationships"></a><span data-ttu-id="ba0dd-142">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ba0dd-142">Relationships</span></span>
<span data-ttu-id="ba0dd-143">Ninguna</span><span class="sxs-lookup"><span data-stu-id="ba0dd-143">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="ba0dd-144">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ba0dd-144">JSON Representation</span></span>
<span data-ttu-id="ba0dd-145">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ba0dd-145">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedDeviceMobileAppConfigurationUserSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfigurationUserSummary",
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



