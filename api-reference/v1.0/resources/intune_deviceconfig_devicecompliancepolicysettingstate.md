# <a name="devicecompliancepolicysettingstate-resource-type"></a><span data-ttu-id="60bf5-101">Tipo de recurso deviceCompliancePolicySettingState</span><span class="sxs-lookup"><span data-stu-id="60bf5-101">deviceCompliancePolicySettingState resource type</span></span>

> <span data-ttu-id="60bf5-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="60bf5-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="60bf5-103">Estados de configuración de directivas de cumplimiento del dispositivo para un dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="60bf5-103">Device Compilance Policy Setting State for a given device.</span></span>
## <a name="properties"></a><span data-ttu-id="60bf5-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="60bf5-104">Properties</span></span>
|<span data-ttu-id="60bf5-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="60bf5-105">Property</span></span>|<span data-ttu-id="60bf5-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="60bf5-106">Type</span></span>|<span data-ttu-id="60bf5-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="60bf5-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="60bf5-108">ajustes</span><span class="sxs-lookup"><span data-stu-id="60bf5-108">setting</span></span>|<span data-ttu-id="60bf5-109">Cadena</span><span class="sxs-lookup"><span data-stu-id="60bf5-109">String</span></span>|<span data-ttu-id="60bf5-110">La configuración que se está notificando</span><span class="sxs-lookup"><span data-stu-id="60bf5-110">The setting that is being reported</span></span>|
|<span data-ttu-id="60bf5-111">settingName</span><span class="sxs-lookup"><span data-stu-id="60bf5-111">settingName</span></span>|<span data-ttu-id="60bf5-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="60bf5-112">String</span></span>|<span data-ttu-id="60bf5-113">Nombre descriptivo de la configuración de usuario o localizada que se está notificando</span><span class="sxs-lookup"><span data-stu-id="60bf5-113">Localized/user friendly setting name that is being reported</span></span>|
|<span data-ttu-id="60bf5-114">instanceDisplayName</span><span class="sxs-lookup"><span data-stu-id="60bf5-114">instanceDisplayName</span></span>|<span data-ttu-id="60bf5-115">Cadena</span><span class="sxs-lookup"><span data-stu-id="60bf5-115">String</span></span>|<span data-ttu-id="60bf5-116">Nombre de la instancia de configuración que se está notificando.</span><span class="sxs-lookup"><span data-stu-id="60bf5-116">Name of setting instance that is being reported.</span></span>|
|<span data-ttu-id="60bf5-117">estado</span><span class="sxs-lookup"><span data-stu-id="60bf5-117">state</span></span>|<span data-ttu-id="60bf5-118">Cadena</span><span class="sxs-lookup"><span data-stu-id="60bf5-118">String</span></span>|<span data-ttu-id="60bf5-119">Estado de cumplimiento de la configuración. Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error` y `conflict`.</span><span class="sxs-lookup"><span data-stu-id="60bf5-119">The compliance state of the setting Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`.</span></span>|
|<span data-ttu-id="60bf5-120">errorCode</span><span class="sxs-lookup"><span data-stu-id="60bf5-120">errorCode</span></span>|<span data-ttu-id="60bf5-121">Int64</span><span class="sxs-lookup"><span data-stu-id="60bf5-121">Int64</span></span>|<span data-ttu-id="60bf5-122">Código de error de la configuración</span><span class="sxs-lookup"><span data-stu-id="60bf5-122">Error code for the setting</span></span>|
|<span data-ttu-id="60bf5-123">errorDescription</span><span class="sxs-lookup"><span data-stu-id="60bf5-123">error_description</span></span>|<span data-ttu-id="60bf5-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="60bf5-124">String</span></span>|<span data-ttu-id="60bf5-125">Descripción del error</span><span class="sxs-lookup"><span data-stu-id="60bf5-125">Error Description</span></span>|
|<span data-ttu-id="60bf5-126">userId</span><span class="sxs-lookup"><span data-stu-id="60bf5-126">userID</span></span>|<span data-ttu-id="60bf5-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="60bf5-127">String</span></span>|<span data-ttu-id="60bf5-128">UserId</span><span class="sxs-lookup"><span data-stu-id="60bf5-128">UserId</span></span>|
|<span data-ttu-id="60bf5-129">userName</span><span class="sxs-lookup"><span data-stu-id="60bf5-129">userName</span></span>|<span data-ttu-id="60bf5-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="60bf5-130">String</span></span>|<span data-ttu-id="60bf5-131">UserName</span><span class="sxs-lookup"><span data-stu-id="60bf5-131">userName</span></span>|
|<span data-ttu-id="60bf5-132">userEmail</span><span class="sxs-lookup"><span data-stu-id="60bf5-132">userEmail</span></span>|<span data-ttu-id="60bf5-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="60bf5-133">String</span></span>|<span data-ttu-id="60bf5-134">UserEmail</span><span class="sxs-lookup"><span data-stu-id="60bf5-134">UserEmail Element</span></span>|
|<span data-ttu-id="60bf5-135">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="60bf5-135">userPrincipalName</span></span>|<span data-ttu-id="60bf5-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="60bf5-136">String</span></span>|<span data-ttu-id="60bf5-137">UserPrincipalName.</span><span class="sxs-lookup"><span data-stu-id="60bf5-137">userPrincipalName</span></span>|
|<span data-ttu-id="60bf5-138">orígenes</span><span class="sxs-lookup"><span data-stu-id="60bf5-138">Sources</span></span>|<span data-ttu-id="60bf5-139">Colección [settingSource](../resources/intune_deviceconfig_settingsource.md)</span><span class="sxs-lookup"><span data-stu-id="60bf5-139">[settingSource](../resources/intune_deviceconfig_settingsource.md) collection</span></span>|<span data-ttu-id="60bf5-140">Directivas colaboradoras</span><span class="sxs-lookup"><span data-stu-id="60bf5-140">Contributing policies</span></span>|
|<span data-ttu-id="60bf5-141">currentValue</span><span class="sxs-lookup"><span data-stu-id="60bf5-141">currentValue</span></span>|<span data-ttu-id="60bf5-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="60bf5-142">String</span></span>|<span data-ttu-id="60bf5-143">Valor actual de la configuración en el dispositivo</span><span class="sxs-lookup"><span data-stu-id="60bf5-143">Current value of setting on device</span></span>|

## <a name="relationships"></a><span data-ttu-id="60bf5-144">Relaciones</span><span class="sxs-lookup"><span data-stu-id="60bf5-144">Relationships</span></span>
<span data-ttu-id="60bf5-145">Ninguna</span><span class="sxs-lookup"><span data-stu-id="60bf5-145">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="60bf5-146">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="60bf5-146">JSON Representation</span></span>
<span data-ttu-id="60bf5-147">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="60bf5-147">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceCompliancePolicySettingState"
}
-->
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



