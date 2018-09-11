# <a name="devicecompliancepolicysettingstate-resource-type"></a><span data-ttu-id="ca29e-101">Tipo de recurso deviceCompliancePolicySettingState</span><span class="sxs-lookup"><span data-stu-id="ca29e-101">deviceCompliancePolicySettingState resource type</span></span>

> <span data-ttu-id="ca29e-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ca29e-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ca29e-103">Estados de configuración de directivas de cumplimiento del dispositivo para un dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="ca29e-103">Device Compilance Policy Setting State for a given device.</span></span>
## <a name="properties"></a><span data-ttu-id="ca29e-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ca29e-104">Properties</span></span>
|<span data-ttu-id="ca29e-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ca29e-105">Property</span></span>|<span data-ttu-id="ca29e-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="ca29e-106">Type</span></span>|<span data-ttu-id="ca29e-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="ca29e-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ca29e-108">setting</span><span class="sxs-lookup"><span data-stu-id="ca29e-108">setting</span></span>|<span data-ttu-id="ca29e-109">Cadena</span><span class="sxs-lookup"><span data-stu-id="ca29e-109">String</span></span>|<span data-ttu-id="ca29e-110">La configuración que se está notificando</span><span class="sxs-lookup"><span data-stu-id="ca29e-110">The setting that is being reported</span></span>|
|<span data-ttu-id="ca29e-111">settingName</span><span class="sxs-lookup"><span data-stu-id="ca29e-111">settingName</span></span>|<span data-ttu-id="ca29e-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="ca29e-112">String</span></span>|<span data-ttu-id="ca29e-113">Nombre descriptivo de la configuración de usuario o localizada que se está notificando</span><span class="sxs-lookup"><span data-stu-id="ca29e-113">Localized/user friendly setting name that is being reported</span></span>|
|<span data-ttu-id="ca29e-114">instanceDisplayName</span><span class="sxs-lookup"><span data-stu-id="ca29e-114">instanceDisplayName</span></span>|<span data-ttu-id="ca29e-115">Cadena</span><span class="sxs-lookup"><span data-stu-id="ca29e-115">String</span></span>|<span data-ttu-id="ca29e-116">Nombre de la instancia de configuración que se está notificando.</span><span class="sxs-lookup"><span data-stu-id="ca29e-116">Name of setting instance that is being reported.</span></span>|
|<span data-ttu-id="ca29e-117">state</span><span class="sxs-lookup"><span data-stu-id="ca29e-117">state</span></span>|[<span data-ttu-id="ca29e-118">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="ca29e-118">complianceStatus</span></span>](../resources/intune_shared_compliancestatus.md)|<span data-ttu-id="ca29e-p101">El estado de cumplimiento de la configuración. Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="ca29e-p101">The compliance state of the setting Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`.</span></span>|
|<span data-ttu-id="ca29e-121">errorCode</span><span class="sxs-lookup"><span data-stu-id="ca29e-121">errorCode</span></span>|<span data-ttu-id="ca29e-122">Int64</span><span class="sxs-lookup"><span data-stu-id="ca29e-122">Int64</span></span>|<span data-ttu-id="ca29e-123">Código de error de la configuración</span><span class="sxs-lookup"><span data-stu-id="ca29e-123">Error code for the setting</span></span>|
|<span data-ttu-id="ca29e-124">errorDescription</span><span class="sxs-lookup"><span data-stu-id="ca29e-124">errorDescription</span></span>|<span data-ttu-id="ca29e-125">Cadena</span><span class="sxs-lookup"><span data-stu-id="ca29e-125">String</span></span>|<span data-ttu-id="ca29e-126">Descripción del error</span><span class="sxs-lookup"><span data-stu-id="ca29e-126">Error description</span></span>|
|<span data-ttu-id="ca29e-127">userId</span><span class="sxs-lookup"><span data-stu-id="ca29e-127">userId</span></span>|<span data-ttu-id="ca29e-128">Cadena</span><span class="sxs-lookup"><span data-stu-id="ca29e-128">String</span></span>|<span data-ttu-id="ca29e-129">UserId</span><span class="sxs-lookup"><span data-stu-id="ca29e-129">UserId</span></span>|
|<span data-ttu-id="ca29e-130">userName</span><span class="sxs-lookup"><span data-stu-id="ca29e-130">userName</span></span>|<span data-ttu-id="ca29e-131">Cadena</span><span class="sxs-lookup"><span data-stu-id="ca29e-131">String</span></span>|<span data-ttu-id="ca29e-132">UserName</span><span class="sxs-lookup"><span data-stu-id="ca29e-132">UserName</span></span>|
|<span data-ttu-id="ca29e-133">userEmail</span><span class="sxs-lookup"><span data-stu-id="ca29e-133">userEmail</span></span>|<span data-ttu-id="ca29e-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="ca29e-134">String</span></span>|<span data-ttu-id="ca29e-135">UserEmail</span><span class="sxs-lookup"><span data-stu-id="ca29e-135">UserEmail</span></span>|
|<span data-ttu-id="ca29e-136">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="ca29e-136">userPrincipalName</span></span>|<span data-ttu-id="ca29e-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="ca29e-137">String</span></span>|<span data-ttu-id="ca29e-138">UserPrincipalName.</span><span class="sxs-lookup"><span data-stu-id="ca29e-138">UserPrincipalName.</span></span>|
|<span data-ttu-id="ca29e-139">sources</span><span class="sxs-lookup"><span data-stu-id="ca29e-139">sources</span></span>|<span data-ttu-id="ca29e-140">Colección [settingSource](../resources/intune_deviceconfig_settingsource.md)</span><span class="sxs-lookup"><span data-stu-id="ca29e-140">[settingSource](../resources/intune_deviceconfig_settingsource.md) collection</span></span>|<span data-ttu-id="ca29e-141">Directivas colaboradoras</span><span class="sxs-lookup"><span data-stu-id="ca29e-141">Contributing policies</span></span>|
|<span data-ttu-id="ca29e-142">currentValue</span><span class="sxs-lookup"><span data-stu-id="ca29e-142">currentValue</span></span>|<span data-ttu-id="ca29e-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="ca29e-143">String</span></span>|<span data-ttu-id="ca29e-144">Valor actual de la configuración en el dispositivo</span><span class="sxs-lookup"><span data-stu-id="ca29e-144">Current value of setting on device</span></span>|

## <a name="relationships"></a><span data-ttu-id="ca29e-145">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ca29e-145">Relationships</span></span>
<span data-ttu-id="ca29e-146">Ninguna</span><span class="sxs-lookup"><span data-stu-id="ca29e-146">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="ca29e-147">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ca29e-147">JSON Representation</span></span>
<span data-ttu-id="ca29e-148">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ca29e-148">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceCompliancePolicySettingState"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceCompliancePolicySettingState",
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








