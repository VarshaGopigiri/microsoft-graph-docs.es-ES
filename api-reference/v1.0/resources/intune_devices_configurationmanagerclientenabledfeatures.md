# <a name="configurationmanagerclientenabledfeatures-resource-type"></a><span data-ttu-id="0eae4-101">Tipo de recurso configurationManagerClientEnabledFeatures</span><span class="sxs-lookup"><span data-stu-id="0eae4-101">configurationManagerClientEnabledFeatures resource type</span></span>

> <span data-ttu-id="0eae4-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0eae4-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0eae4-103">Características habilitadas del cliente de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="0eae4-103">configuration Manager client enabled features</span></span>
## <a name="properties"></a><span data-ttu-id="0eae4-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0eae4-104">Properties</span></span>
|<span data-ttu-id="0eae4-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0eae4-105">Property</span></span>|<span data-ttu-id="0eae4-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="0eae4-106">Type</span></span>|<span data-ttu-id="0eae4-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="0eae4-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0eae4-108">inventario</span><span class="sxs-lookup"><span data-stu-id="0eae4-108">inventory</span></span>|<span data-ttu-id="0eae4-109">Booleano</span><span class="sxs-lookup"><span data-stu-id="0eae4-109">Boolean</span></span>|<span data-ttu-id="0eae4-110">Si el inventario se administra con Intune</span><span class="sxs-lookup"><span data-stu-id="0eae4-110">Whether inventory is managed by Intune</span></span>|
|<span data-ttu-id="0eae4-111">modernApps</span><span class="sxs-lookup"><span data-stu-id="0eae4-111">modernApps</span></span>|<span data-ttu-id="0eae4-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="0eae4-112">Boolean</span></span>|<span data-ttu-id="0eae4-113">Si la aplicación moderna se administra con Intune</span><span class="sxs-lookup"><span data-stu-id="0eae4-113">Whether modern application is managed by Intune</span></span>|
|<span data-ttu-id="0eae4-114">resourceAccess</span><span class="sxs-lookup"><span data-stu-id="0eae4-114">resourceAccess</span></span>|<span data-ttu-id="0eae4-115">Booleano</span><span class="sxs-lookup"><span data-stu-id="0eae4-115">Boolean</span></span>|<span data-ttu-id="0eae4-116">Si el acceso a los recursos se administra con Intune</span><span class="sxs-lookup"><span data-stu-id="0eae4-116">Whether resource access is managed by Intune</span></span>|
|<span data-ttu-id="0eae4-117">deviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="0eae4-117">deviceConfiguration</span></span>|<span data-ttu-id="0eae4-118">Booleano</span><span class="sxs-lookup"><span data-stu-id="0eae4-118">Boolean</span></span>|<span data-ttu-id="0eae4-119">Si la configuración de dispositivos se administra con Intune</span><span class="sxs-lookup"><span data-stu-id="0eae4-119">Whether device configuration is managed by Intune</span></span>|
|<span data-ttu-id="0eae4-120">compliancePolicy</span><span class="sxs-lookup"><span data-stu-id="0eae4-120">compliancePolicy</span></span>|<span data-ttu-id="0eae4-121">Booleano</span><span class="sxs-lookup"><span data-stu-id="0eae4-121">Boolean</span></span>|<span data-ttu-id="0eae4-122">Si la directiva de cumplimiento se administra con Intune</span><span class="sxs-lookup"><span data-stu-id="0eae4-122">Whether compliance policy is managed by Intune</span></span>|
|<span data-ttu-id="0eae4-123">windowsUpdateForBusiness</span><span class="sxs-lookup"><span data-stu-id="0eae4-123">windowsUpdateForBusiness</span></span>|<span data-ttu-id="0eae4-124">Booleano</span><span class="sxs-lookup"><span data-stu-id="0eae4-124">Boolean</span></span>|<span data-ttu-id="0eae4-125">Si Windows Update para empresas se administra con Intune</span><span class="sxs-lookup"><span data-stu-id="0eae4-125">Whether Windows Update for Business is managed by Intune</span></span>|

## <a name="relationships"></a><span data-ttu-id="0eae4-126">Relaciones</span><span class="sxs-lookup"><span data-stu-id="0eae4-126">Relationships</span></span>
<span data-ttu-id="0eae4-127">Ninguna</span><span class="sxs-lookup"><span data-stu-id="0eae4-127">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="0eae4-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0eae4-128">JSON Representation</span></span>
<span data-ttu-id="0eae4-129">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="0eae4-129">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.configurationManagerClientEnabledFeatures"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.configurationManagerClientEnabledFeatures",
  "inventory": true,
  "modernApps": true,
  "resourceAccess": true,
  "deviceConfiguration": true,
  "compliancePolicy": true,
  "windowsUpdateForBusiness": true
}
```



