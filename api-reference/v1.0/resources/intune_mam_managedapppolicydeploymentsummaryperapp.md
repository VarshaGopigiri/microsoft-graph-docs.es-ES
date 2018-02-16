# <a name="managedapppolicydeploymentsummaryperapp-resource-type"></a><span data-ttu-id="cf1a0-101">Tipo de recurso managedAppPolicyDeploymentSummaryPerApp</span><span class="sxs-lookup"><span data-stu-id="cf1a0-101">managedAppPolicyDeploymentSummaryPerApp resource type</span></span>

> <span data-ttu-id="cf1a0-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cf1a0-103">Representa el resumen de implementación de directivas por aplicación.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-103">Represents policy deployment summary per app.</span></span>
## <a name="properties"></a><span data-ttu-id="cf1a0-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cf1a0-104">Properties</span></span>
|<span data-ttu-id="cf1a0-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cf1a0-105">Property</span></span>|<span data-ttu-id="cf1a0-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf1a0-106">Type</span></span>|<span data-ttu-id="cf1a0-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf1a0-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="cf1a0-108">mobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="cf1a0-108">mobileAppIdentifier</span></span>|[<span data-ttu-id="cf1a0-109">mobileAppIdentifier</span><span class="sxs-lookup"><span data-stu-id="cf1a0-109">mobileAppIdentifier</span></span>](../resources/intune_mam_mobileappidentifier.md)|<span data-ttu-id="cf1a0-110">Implementación de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-110">Deployment of an app.</span></span>|
|<span data-ttu-id="cf1a0-111">configurationAppliedUserCount</span><span class="sxs-lookup"><span data-stu-id="cf1a0-111">configurationAppliedUserCount</span></span>|<span data-ttu-id="cf1a0-112">Int32</span><span class="sxs-lookup"><span data-stu-id="cf1a0-112">Int32</span></span>|<span data-ttu-id="cf1a0-113">Número de usuarios a los que se aplica la directiva.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-113">Number of users the policy is applied.</span></span>|

## <a name="relationships"></a><span data-ttu-id="cf1a0-114">Relaciones</span><span class="sxs-lookup"><span data-stu-id="cf1a0-114">Relationships</span></span>
<span data-ttu-id="cf1a0-115">Ninguna</span><span class="sxs-lookup"><span data-stu-id="cf1a0-115">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="cf1a0-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="cf1a0-116">JSON Representation</span></span>
<span data-ttu-id="cf1a0-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="cf1a0-117">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedAppPolicyDeploymentSummaryPerApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAppPolicyDeploymentSummaryPerApp",
  "mobileAppIdentifier": {
    "@odata.type": "microsoft.graph.mobileAppIdentifier"
  },
  "configurationAppliedUserCount": 1024
}
```



