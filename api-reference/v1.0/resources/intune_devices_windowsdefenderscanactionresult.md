# <a name="windowsdefenderscanactionresult-resource-type"></a><span data-ttu-id="6a354-101">Tipo de recurso windowsDefenderScanActionResult</span><span class="sxs-lookup"><span data-stu-id="6a354-101">windowsDefenderScanActionResult resource type</span></span>

> <span data-ttu-id="6a354-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6a354-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6a354-103">Resultado del último análisis de Windows Defender</span><span class="sxs-lookup"><span data-stu-id="6a354-103">Windows Defender last scan result</span></span>

<span data-ttu-id="6a354-104">Hereda de [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="6a354-104">Inherits from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>

## <a name="properties"></a><span data-ttu-id="6a354-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6a354-105">Properties</span></span>
|<span data-ttu-id="6a354-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6a354-106">Property</span></span>|<span data-ttu-id="6a354-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="6a354-107">Type</span></span>|<span data-ttu-id="6a354-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a354-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6a354-109">actionName</span><span class="sxs-lookup"><span data-stu-id="6a354-109">actionName</span></span>|<span data-ttu-id="6a354-110">cadena</span><span class="sxs-lookup"><span data-stu-id="6a354-110">String</span></span>|<span data-ttu-id="6a354-111">Nombre de la acción. Heredado de [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="6a354-111">Action name Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>|
|<span data-ttu-id="6a354-112">actionState</span><span class="sxs-lookup"><span data-stu-id="6a354-112">actionState</span></span>|[<span data-ttu-id="6a354-113">actionState</span><span class="sxs-lookup"><span data-stu-id="6a354-113">actionState</span></span>](../resources/intune_devices_actionstate.md)|<span data-ttu-id="6a354-114">Estado de la acción Inherited desde [deviceActionResult](../resources/intune_devices_deviceactionresult.md).</span><span class="sxs-lookup"><span data-stu-id="6a354-114">State of the action Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md).</span></span> <span data-ttu-id="6a354-115">Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="6a354-115">Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="6a354-116">startDateTime</span><span class="sxs-lookup"><span data-stu-id="6a354-116">startDateTime</span></span>|<span data-ttu-id="6a354-117">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6a354-117">DateTimeOffset</span></span>|<span data-ttu-id="6a354-118">Hora en la que se inició la acción. Heredado de [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="6a354-118">Time the action was initiated Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>|
|<span data-ttu-id="6a354-119">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="6a354-119">lastUpdatedDateTime</span></span>|<span data-ttu-id="6a354-120">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="6a354-120">DateTimeOffset</span></span>|<span data-ttu-id="6a354-121">Hora en la que se actualizó por última vez el estado de acción. Heredado de [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="6a354-121">Time the action state was last updated Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>|
|<span data-ttu-id="6a354-122">scanType</span><span class="sxs-lookup"><span data-stu-id="6a354-122">scanType</span></span>|<span data-ttu-id="6a354-123">cadena</span><span class="sxs-lookup"><span data-stu-id="6a354-123">String</span></span>|<span data-ttu-id="6a354-124">Tipo de análisis, sea análisis completo o análisis rápido</span><span class="sxs-lookup"><span data-stu-id="6a354-124">Scan type either full scan or quick scan</span></span>|

## <a name="relationships"></a><span data-ttu-id="6a354-125">Relaciones</span><span class="sxs-lookup"><span data-stu-id="6a354-125">Relationships</span></span>
<span data-ttu-id="6a354-126">Ninguna</span><span class="sxs-lookup"><span data-stu-id="6a354-126">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="6a354-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6a354-127">JSON Representation</span></span>
<span data-ttu-id="6a354-128">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="6a354-128">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsDefenderScanActionResult"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsDefenderScanActionResult",
  "actionName": "String",
  "actionState": "String",
  "startDateTime": "String (timestamp)",
  "lastUpdatedDateTime": "String (timestamp)",
  "scanType": "String"
}
```



