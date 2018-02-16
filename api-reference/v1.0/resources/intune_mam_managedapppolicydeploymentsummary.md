# <a name="managedapppolicydeploymentsummary-resource-type"></a><span data-ttu-id="43bfa-101">Tipo de recurso managedAppPolicyDeploymentSummary</span><span class="sxs-lookup"><span data-stu-id="43bfa-101">managedAppPolicyDeploymentSummary resource type</span></span>

> <span data-ttu-id="43bfa-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="43bfa-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="43bfa-103">El objeto ManagedAppEntity es el tipo de entidad base para todos los demás tipos de entidad en flujos de trabajo de administración de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="43bfa-103">The ManagedAppEntity is the base entity type for all other entity types under app management workflow.</span></span>
## <a name="methods"></a><span data-ttu-id="43bfa-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="43bfa-104">Methods</span></span>
|<span data-ttu-id="43bfa-105">Método</span><span class="sxs-lookup"><span data-stu-id="43bfa-105">Method</span></span>|<span data-ttu-id="43bfa-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="43bfa-106">Return Type</span></span>|<span data-ttu-id="43bfa-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="43bfa-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="43bfa-108">Obtener managedAppPolicyDeploymentSummary</span><span class="sxs-lookup"><span data-stu-id="43bfa-108">Get managedAppPolicyDeploymentSummary</span></span>](../api/intune_mam_managedapppolicydeploymentsummary_get.md)|[<span data-ttu-id="43bfa-109">managedAppPolicyDeploymentSummary</span><span class="sxs-lookup"><span data-stu-id="43bfa-109">managedAppPolicyDeploymentSummary</span></span>](../resources/intune_mam_managedapppolicydeploymentsummary.md)|<span data-ttu-id="43bfa-110">Lea las propiedades y las relaciones del objeto [managedAppPolicyDeploymentSummary](../resources/intune_mam_managedapppolicydeploymentsummary.md).</span><span class="sxs-lookup"><span data-stu-id="43bfa-110">Read properties and relationships of [plannerTaskDetails](../resources/intune_mam_managedapppolicydeploymentsummary.md) object.</span></span>|
|[<span data-ttu-id="43bfa-111">Actualizar managedAppPolicyDeploymentSummary</span><span class="sxs-lookup"><span data-stu-id="43bfa-111">Update managedAppPolicyDeploymentSummary</span></span>](../api/intune_mam_managedapppolicydeploymentsummary_update.md)|[<span data-ttu-id="43bfa-112">managedAppPolicyDeploymentSummary</span><span class="sxs-lookup"><span data-stu-id="43bfa-112">managedAppPolicyDeploymentSummary</span></span>](../resources/intune_mam_managedapppolicydeploymentsummary.md)|<span data-ttu-id="43bfa-113">Actualice las propiedades de un objeto [managedAppPolicyDeploymentSummary](../resources/intune_mam_managedapppolicydeploymentsummary.md).</span><span class="sxs-lookup"><span data-stu-id="43bfa-113">Update the properties of a [calendar](../resources/intune_mam_managedapppolicydeploymentsummary.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="43bfa-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="43bfa-114">Properties</span></span>
|<span data-ttu-id="43bfa-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="43bfa-115">Property</span></span>|<span data-ttu-id="43bfa-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="43bfa-116">Type</span></span>|<span data-ttu-id="43bfa-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="43bfa-117">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="43bfa-118">displayName</span><span class="sxs-lookup"><span data-stu-id="43bfa-118">displayName</span></span>|<span data-ttu-id="43bfa-119">cadena</span><span class="sxs-lookup"><span data-stu-id="43bfa-119">String</span></span>|<span data-ttu-id="43bfa-120">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="43bfa-120">Not yet documented</span></span>|
|<span data-ttu-id="43bfa-121">configurationDeployedUserCount</span><span class="sxs-lookup"><span data-stu-id="43bfa-121">configurationDeployedUserCount</span></span>|<span data-ttu-id="43bfa-122">Int32</span><span class="sxs-lookup"><span data-stu-id="43bfa-122">Int32</span></span>|<span data-ttu-id="43bfa-123">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="43bfa-123">Not yet documented</span></span>|
|<span data-ttu-id="43bfa-124">lastRefreshTime</span><span class="sxs-lookup"><span data-stu-id="43bfa-124">lastRefreshTime</span></span>|<span data-ttu-id="43bfa-125">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="43bfa-125">DateTimeOffset</span></span>|<span data-ttu-id="43bfa-126">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="43bfa-126">Not yet documented</span></span>|
|<span data-ttu-id="43bfa-127">configurationDeploymentSummaryPerApp</span><span class="sxs-lookup"><span data-stu-id="43bfa-127">configurationDeploymentSummaryPerApp</span></span>|<span data-ttu-id="43bfa-128">Colección [managedAppPolicyDeploymentSummaryPerApp](../resources/intune_mam_managedapppolicydeploymentsummaryperapp.md)</span><span class="sxs-lookup"><span data-stu-id="43bfa-128">[managedAppPolicyDeploymentSummaryPerApp](../resources/intune_mam_managedapppolicydeploymentsummaryperapp.md) collection</span></span>|<span data-ttu-id="43bfa-129">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="43bfa-129">Not yet documented</span></span>|
|<span data-ttu-id="43bfa-130">id</span><span class="sxs-lookup"><span data-stu-id="43bfa-130">id</span></span>|<span data-ttu-id="43bfa-131">cadena</span><span class="sxs-lookup"><span data-stu-id="43bfa-131">String</span></span>|<span data-ttu-id="43bfa-132">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="43bfa-132">Key of the setting.</span></span>|
|<span data-ttu-id="43bfa-133">versión</span><span class="sxs-lookup"><span data-stu-id="43bfa-133">version</span></span>|<span data-ttu-id="43bfa-134">cadena</span><span class="sxs-lookup"><span data-stu-id="43bfa-134">String</span></span>|<span data-ttu-id="43bfa-135">Versión de la entidad.</span><span class="sxs-lookup"><span data-stu-id="43bfa-135">Version of the entity.</span></span>|

## <a name="relationships"></a><span data-ttu-id="43bfa-136">Relaciones</span><span class="sxs-lookup"><span data-stu-id="43bfa-136">Relationships</span></span>
<span data-ttu-id="43bfa-137">Ninguna</span><span class="sxs-lookup"><span data-stu-id="43bfa-137">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="43bfa-138">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="43bfa-138">JSON Representation</span></span>
<span data-ttu-id="43bfa-139">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="43bfa-139">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedAppPolicyDeploymentSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAppPolicyDeploymentSummary",
  "displayName": "String",
  "configurationDeployedUserCount": 1024,
  "lastRefreshTime": "String (timestamp)",
  "configurationDeploymentSummaryPerApp": [
    {
      "@odata.type": "microsoft.graph.managedAppPolicyDeploymentSummaryPerApp",
      "mobileAppIdentifier": {
        "@odata.type": "microsoft.graph.androidMobileAppIdentifier",
        "packageId": "String"
      },
      "configurationAppliedUserCount": 1024
    }
  ],
  "id": "String (identifier)",
  "version": "String"
}
```



