# <a name="deviceconfigurationsettingstate-resource-type"></a><span data-ttu-id="9ec93-101">Tipo de recurso deviceConfigurationSettingState</span><span class="sxs-lookup"><span data-stu-id="9ec93-101">deviceConfigurationSettingState resource type</span></span>

> <span data-ttu-id="9ec93-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9ec93-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9ec93-103">Estado de la configuración de dispositivos de un dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="9ec93-103">Device Configuration Setting State for a given device.</span></span>
## <a name="properties"></a><span data-ttu-id="9ec93-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9ec93-104">Properties</span></span>
|<span data-ttu-id="9ec93-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9ec93-105">Property</span></span>|<span data-ttu-id="9ec93-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="9ec93-106">Type</span></span>|<span data-ttu-id="9ec93-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="9ec93-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9ec93-108">ajustes</span><span class="sxs-lookup"><span data-stu-id="9ec93-108">setting</span></span>|<span data-ttu-id="9ec93-109">cadena</span><span class="sxs-lookup"><span data-stu-id="9ec93-109">String</span></span>|<span data-ttu-id="9ec93-110">La configuración que se está notificando</span><span class="sxs-lookup"><span data-stu-id="9ec93-110">The setting that is being reported</span></span>|
|<span data-ttu-id="9ec93-111">settingName</span><span class="sxs-lookup"><span data-stu-id="9ec93-111">settingName</span></span>|<span data-ttu-id="9ec93-112">cadena</span><span class="sxs-lookup"><span data-stu-id="9ec93-112">String</span></span>|<span data-ttu-id="9ec93-113">Nombre descriptivo de la configuración de usuario o localizada que se está notificando</span><span class="sxs-lookup"><span data-stu-id="9ec93-113">Localized/user friendly setting name that is being reported</span></span>|
|<span data-ttu-id="9ec93-114">instanceDisplayName</span><span class="sxs-lookup"><span data-stu-id="9ec93-114">instanceDisplayName</span></span>|<span data-ttu-id="9ec93-115">cadena</span><span class="sxs-lookup"><span data-stu-id="9ec93-115">String</span></span>|<span data-ttu-id="9ec93-116">Nombre de la instancia de configuración que se está notificando.</span><span class="sxs-lookup"><span data-stu-id="9ec93-116">Name of setting instance that is being reported.</span></span>|
|<span data-ttu-id="9ec93-117">estado</span><span class="sxs-lookup"><span data-stu-id="9ec93-117">state</span></span>|[<span data-ttu-id="9ec93-118">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="9ec93-118">complianceStatus</span></span>](../resources/intune_shared_compliancestatus.md)|<span data-ttu-id="9ec93-119">El estado de cumplimiento de la configuración.</span><span class="sxs-lookup"><span data-stu-id="9ec93-119">The compliance state of the setting.</span></span> <span data-ttu-id="9ec93-120">Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="9ec93-120">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span></span>|
|<span data-ttu-id="9ec93-121">errorCode</span><span class="sxs-lookup"><span data-stu-id="9ec93-121">errorCode</span></span>|<span data-ttu-id="9ec93-122">Int64</span><span class="sxs-lookup"><span data-stu-id="9ec93-122">Int64</span></span>|<span data-ttu-id="9ec93-123">Código de error de la configuración</span><span class="sxs-lookup"><span data-stu-id="9ec93-123">Error code for the setting</span></span>|
|<span data-ttu-id="9ec93-124">errorDescription</span><span class="sxs-lookup"><span data-stu-id="9ec93-124">errorDescription</span></span>|<span data-ttu-id="9ec93-125">Cadena</span><span class="sxs-lookup"><span data-stu-id="9ec93-125">String</span></span>|<span data-ttu-id="9ec93-126">Descripción del error</span><span class="sxs-lookup"><span data-stu-id="9ec93-126">Error description</span></span>|
|<span data-ttu-id="9ec93-127">userId</span><span class="sxs-lookup"><span data-stu-id="9ec93-127">userId</span></span>|<span data-ttu-id="9ec93-128">Cadena</span><span class="sxs-lookup"><span data-stu-id="9ec93-128">String</span></span>|<span data-ttu-id="9ec93-129">UserId</span><span class="sxs-lookup"><span data-stu-id="9ec93-129">UserId</span></span>|
|<span data-ttu-id="9ec93-130">userName</span><span class="sxs-lookup"><span data-stu-id="9ec93-130">userName</span></span>|<span data-ttu-id="9ec93-131">Cadena</span><span class="sxs-lookup"><span data-stu-id="9ec93-131">String</span></span>|<span data-ttu-id="9ec93-132">UserName</span><span class="sxs-lookup"><span data-stu-id="9ec93-132">UserName</span></span>|
|<span data-ttu-id="9ec93-133">userEmail</span><span class="sxs-lookup"><span data-stu-id="9ec93-133">userEmail</span></span>|<span data-ttu-id="9ec93-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="9ec93-134">String</span></span>|<span data-ttu-id="9ec93-135">UserEmail</span><span class="sxs-lookup"><span data-stu-id="9ec93-135">UserEmail</span></span>|
|<span data-ttu-id="9ec93-136">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="9ec93-136">userPrincipalName</span></span>|<span data-ttu-id="9ec93-137">String</span><span class="sxs-lookup"><span data-stu-id="9ec93-137">String</span></span>|<span data-ttu-id="9ec93-138">UserPrincipalName.</span><span class="sxs-lookup"><span data-stu-id="9ec93-138">UserPrincipalName.</span></span>|
|<span data-ttu-id="9ec93-139">orígenes</span><span class="sxs-lookup"><span data-stu-id="9ec93-139">sources</span></span>|<span data-ttu-id="9ec93-140">Colección [settingSource](../resources/intune_deviceconfig_settingsource.md)</span><span class="sxs-lookup"><span data-stu-id="9ec93-140">[settingSource](../resources/intune_deviceconfig_settingsource.md) collection</span></span>|<span data-ttu-id="9ec93-141">Directivas colaboradoras</span><span class="sxs-lookup"><span data-stu-id="9ec93-141">Contributing policies</span></span>|
|<span data-ttu-id="9ec93-142">currentValue</span><span class="sxs-lookup"><span data-stu-id="9ec93-142">currentValue</span></span>|<span data-ttu-id="9ec93-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="9ec93-143">String</span></span>|<span data-ttu-id="9ec93-144">Valor actual de la configuración en el dispositivo</span><span class="sxs-lookup"><span data-stu-id="9ec93-144">Current value of setting on device</span></span>|

## <a name="relationships"></a><span data-ttu-id="9ec93-145">Relaciones</span><span class="sxs-lookup"><span data-stu-id="9ec93-145">Relationships</span></span>
<span data-ttu-id="9ec93-146">Ninguna</span><span class="sxs-lookup"><span data-stu-id="9ec93-146">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="9ec93-147">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9ec93-147">JSON Representation</span></span>
<span data-ttu-id="9ec93-148">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="9ec93-148">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceConfigurationSettingState"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceConfigurationSettingState",
  "setting": "String",
  "settingName": "String",
  "instanceDisplayName": "String",
  "state": "String",
  "errorCode": 1024,
  "errorDescription": "String",
  "userId": "String",
  "userName": "String",
  "userEmail": "String",
  "userPrincipalName": "String",
  "sources": [
    {
      "@odata.type": "microsoft.graph.settingSource",
      "id": "String",
      "displayName": "String"
    }
  ],
  "currentValue": "String"
}
```



