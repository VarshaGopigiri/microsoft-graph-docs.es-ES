# <a name="windowsdefenderscanactionresult-resource-type"></a><span data-ttu-id="53d89-101">Tipo de recurso windowsDefenderScanActionResult</span><span class="sxs-lookup"><span data-stu-id="53d89-101">windowsDefenderScanActionResult resource type</span></span>

> <span data-ttu-id="53d89-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="53d89-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="53d89-103">Resultado del último análisis de Windows Defender</span><span class="sxs-lookup"><span data-stu-id="53d89-103">Windows Defender last scan result</span></span>

<span data-ttu-id="53d89-104">Hereda de [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="53d89-104">Inherits from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>

## <a name="properties"></a><span data-ttu-id="53d89-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="53d89-105">Properties</span></span>
|<span data-ttu-id="53d89-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="53d89-106">Property</span></span>|<span data-ttu-id="53d89-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="53d89-107">Type</span></span>|<span data-ttu-id="53d89-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="53d89-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="53d89-109">actionName</span><span class="sxs-lookup"><span data-stu-id="53d89-109">actionName</span></span>|<span data-ttu-id="53d89-110">cadena</span><span class="sxs-lookup"><span data-stu-id="53d89-110">String</span></span>|<span data-ttu-id="53d89-111">Nombre de la acción. Heredado de [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="53d89-111">Action name Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>|
|<span data-ttu-id="53d89-112">actionState</span><span class="sxs-lookup"><span data-stu-id="53d89-112">actionState</span></span>|<span data-ttu-id="53d89-113">cadena</span><span class="sxs-lookup"><span data-stu-id="53d89-113">String</span></span>|<span data-ttu-id="53d89-114">Estado de la acción. Heredado de [deviceActionResult](../resources/intune_devices_deviceactionresult.md). Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="53d89-114">State of the action Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md) Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="53d89-115">startDateTime</span><span class="sxs-lookup"><span data-stu-id="53d89-115">startDateTime</span></span>|<span data-ttu-id="53d89-116">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="53d89-116">DateTimeOffset</span></span>|<span data-ttu-id="53d89-117">Hora en la que se inició la acción. Heredado de [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="53d89-117">Time the action was initiated Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>|
|<span data-ttu-id="53d89-118">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="53d89-118">lastUpdatedDateTime</span></span>|<span data-ttu-id="53d89-119">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="53d89-119">DateTimeOffset</span></span>|<span data-ttu-id="53d89-120">Hora en la que se actualizó por última vez el estado de acción. Heredado de [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="53d89-120">Time the action state was last updated Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>|
|<span data-ttu-id="53d89-121">scanType</span><span class="sxs-lookup"><span data-stu-id="53d89-121">scanType</span></span>|<span data-ttu-id="53d89-122">cadena</span><span class="sxs-lookup"><span data-stu-id="53d89-122">String</span></span>|<span data-ttu-id="53d89-123">Tipo de análisis, sea análisis completo o análisis rápido</span><span class="sxs-lookup"><span data-stu-id="53d89-123">Scan type either full scan or quick scan</span></span>|

## <a name="relationships"></a><span data-ttu-id="53d89-124">Relaciones</span><span class="sxs-lookup"><span data-stu-id="53d89-124">Relationships</span></span>
<span data-ttu-id="53d89-125">Ninguna</span><span class="sxs-lookup"><span data-stu-id="53d89-125">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="53d89-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="53d89-126">JSON Representation</span></span>
<span data-ttu-id="53d89-127">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="53d89-127">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
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



