# <a name="deviceconfigurationsettingstate-resource-type"></a><span data-ttu-id="f49b9-101">Tipo de recurso deviceConfigurationSettingState</span><span class="sxs-lookup"><span data-stu-id="f49b9-101">deviceConfigurationSettingState resource type</span></span>

> <span data-ttu-id="f49b9-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f49b9-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f49b9-103">Estado de la configuración de dispositivos de un dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="f49b9-103">Device Configuration Setting State for a given device.</span></span>
## <a name="properties"></a><span data-ttu-id="f49b9-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f49b9-104">Properties</span></span>
|<span data-ttu-id="f49b9-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f49b9-105">Property</span></span>|<span data-ttu-id="f49b9-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="f49b9-106">Type</span></span>|<span data-ttu-id="f49b9-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="f49b9-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f49b9-108">ajustes</span><span class="sxs-lookup"><span data-stu-id="f49b9-108">setting</span></span>|<span data-ttu-id="f49b9-109">cadena</span><span class="sxs-lookup"><span data-stu-id="f49b9-109">String</span></span>|<span data-ttu-id="f49b9-110">La configuración que se está notificando</span><span class="sxs-lookup"><span data-stu-id="f49b9-110">The setting that is being reported</span></span>|
|<span data-ttu-id="f49b9-111">settingName</span><span class="sxs-lookup"><span data-stu-id="f49b9-111">settingName</span></span>|<span data-ttu-id="f49b9-112">cadena</span><span class="sxs-lookup"><span data-stu-id="f49b9-112">String</span></span>|<span data-ttu-id="f49b9-113">Nombre descriptivo de la configuración de usuario o localizada que se está notificando</span><span class="sxs-lookup"><span data-stu-id="f49b9-113">Localized/user friendly setting name that is being reported</span></span>|
|<span data-ttu-id="f49b9-114">instanceDisplayName</span><span class="sxs-lookup"><span data-stu-id="f49b9-114">instanceDisplayName</span></span>|<span data-ttu-id="f49b9-115">cadena</span><span class="sxs-lookup"><span data-stu-id="f49b9-115">String</span></span>|<span data-ttu-id="f49b9-116">Nombre de la instancia de configuración que se está notificando.</span><span class="sxs-lookup"><span data-stu-id="f49b9-116">Name of setting instance that is being reported.</span></span>|
|<span data-ttu-id="f49b9-117">estado</span><span class="sxs-lookup"><span data-stu-id="f49b9-117">state</span></span>|<span data-ttu-id="f49b9-118">cadena</span><span class="sxs-lookup"><span data-stu-id="f49b9-118">String</span></span>|<span data-ttu-id="f49b9-119">Estado de cumplimiento de la configuración. Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error` y `conflict`.</span><span class="sxs-lookup"><span data-stu-id="f49b9-119">The compliance state of the setting Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`.</span></span>|
|<span data-ttu-id="f49b9-120">errorCode</span><span class="sxs-lookup"><span data-stu-id="f49b9-120">errorCode</span></span>|<span data-ttu-id="f49b9-121">Int64</span><span class="sxs-lookup"><span data-stu-id="f49b9-121">Int64</span></span>|<span data-ttu-id="f49b9-122">Código de error de la configuración</span><span class="sxs-lookup"><span data-stu-id="f49b9-122">Error code for the setting</span></span>|
|<span data-ttu-id="f49b9-123">errorDescription</span><span class="sxs-lookup"><span data-stu-id="f49b9-123">error_description</span></span>|<span data-ttu-id="f49b9-124">cadena</span><span class="sxs-lookup"><span data-stu-id="f49b9-124">String</span></span>|<span data-ttu-id="f49b9-125">Descripción del error</span><span class="sxs-lookup"><span data-stu-id="f49b9-125">Error Description</span></span>|
|<span data-ttu-id="f49b9-126">userId</span><span class="sxs-lookup"><span data-stu-id="f49b9-126">userID</span></span>|<span data-ttu-id="f49b9-127">cadena</span><span class="sxs-lookup"><span data-stu-id="f49b9-127">String</span></span>|<span data-ttu-id="f49b9-128">UserId</span><span class="sxs-lookup"><span data-stu-id="f49b9-128">UserId</span></span>|
|<span data-ttu-id="f49b9-129">userName</span><span class="sxs-lookup"><span data-stu-id="f49b9-129">userName</span></span>|<span data-ttu-id="f49b9-130">cadena</span><span class="sxs-lookup"><span data-stu-id="f49b9-130">String</span></span>|<span data-ttu-id="f49b9-131">UserName</span><span class="sxs-lookup"><span data-stu-id="f49b9-131">userName</span></span>|
|<span data-ttu-id="f49b9-132">userEmail</span><span class="sxs-lookup"><span data-stu-id="f49b9-132">userEmail</span></span>|<span data-ttu-id="f49b9-133">cadena</span><span class="sxs-lookup"><span data-stu-id="f49b9-133">String</span></span>|<span data-ttu-id="f49b9-134">UserEmail</span><span class="sxs-lookup"><span data-stu-id="f49b9-134">UserEmail Element</span></span>|
|<span data-ttu-id="f49b9-135">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="f49b9-135">userPrincipalName</span></span>|<span data-ttu-id="f49b9-136">cadena</span><span class="sxs-lookup"><span data-stu-id="f49b9-136">String</span></span>|<span data-ttu-id="f49b9-137">UserPrincipalName.</span><span class="sxs-lookup"><span data-stu-id="f49b9-137">userPrincipalName</span></span>|
|<span data-ttu-id="f49b9-138">orígenes</span><span class="sxs-lookup"><span data-stu-id="f49b9-138">Sources</span></span>|<span data-ttu-id="f49b9-139">Colección [settingSource](../resources/intune_deviceconfig_settingsource.md)</span><span class="sxs-lookup"><span data-stu-id="f49b9-139">[settingSource](../resources/intune_deviceconfig_settingsource.md) collection</span></span>|<span data-ttu-id="f49b9-140">Directivas colaboradoras</span><span class="sxs-lookup"><span data-stu-id="f49b9-140">Contributing policies</span></span>|
|<span data-ttu-id="f49b9-141">currentValue</span><span class="sxs-lookup"><span data-stu-id="f49b9-141">currentValue</span></span>|<span data-ttu-id="f49b9-142">cadena</span><span class="sxs-lookup"><span data-stu-id="f49b9-142">String</span></span>|<span data-ttu-id="f49b9-143">Valor actual de la configuración en el dispositivo</span><span class="sxs-lookup"><span data-stu-id="f49b9-143">Current value of setting on device</span></span>|

## <a name="relationships"></a><span data-ttu-id="f49b9-144">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f49b9-144">Relationships</span></span>
<span data-ttu-id="f49b9-145">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f49b9-145">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="f49b9-146">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f49b9-146">JSON Representation</span></span>
<span data-ttu-id="f49b9-147">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f49b9-147">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
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



