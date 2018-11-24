# <a name="locatedeviceactionresult-resource-type"></a><span data-ttu-id="92e30-101">Tipo de recurso locateDeviceActionResult</span><span class="sxs-lookup"><span data-stu-id="92e30-101">locateDeviceActionResult resource type</span></span>

> <span data-ttu-id="92e30-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="92e30-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="92e30-103">Resultado de la acción Buscar dispositivo</span><span class="sxs-lookup"><span data-stu-id="92e30-103">Locate device action result</span></span>

<span data-ttu-id="92e30-104">Hereda de [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="92e30-104">Inherits from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>

## <a name="properties"></a><span data-ttu-id="92e30-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="92e30-105">Properties</span></span>
|<span data-ttu-id="92e30-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="92e30-106">Property</span></span>|<span data-ttu-id="92e30-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="92e30-107">Type</span></span>|<span data-ttu-id="92e30-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="92e30-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="92e30-109">actionName</span><span class="sxs-lookup"><span data-stu-id="92e30-109">actionName</span></span>|<span data-ttu-id="92e30-110">cadena</span><span class="sxs-lookup"><span data-stu-id="92e30-110">String</span></span>|<span data-ttu-id="92e30-111">Nombre de la acción. Heredado de [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="92e30-111">Action name Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>|
|<span data-ttu-id="92e30-112">actionState</span><span class="sxs-lookup"><span data-stu-id="92e30-112">actionState</span></span>|[<span data-ttu-id="92e30-113">actionState</span><span class="sxs-lookup"><span data-stu-id="92e30-113">actionState</span></span>](../resources/intune_devices_actionstate.md)|<span data-ttu-id="92e30-114">Estado de la acción Inherited desde [deviceActionResult](../resources/intune_devices_deviceactionresult.md).</span><span class="sxs-lookup"><span data-stu-id="92e30-114">State of the action Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md).</span></span> <span data-ttu-id="92e30-115">Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="92e30-115">Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="92e30-116">startDateTime</span><span class="sxs-lookup"><span data-stu-id="92e30-116">startDateTime</span></span>|<span data-ttu-id="92e30-117">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="92e30-117">DateTimeOffset</span></span>|<span data-ttu-id="92e30-118">Hora en la que se inició la acción. Heredado de [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="92e30-118">Time the action was initiated Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>|
|<span data-ttu-id="92e30-119">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="92e30-119">lastUpdatedDateTime</span></span>|<span data-ttu-id="92e30-120">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="92e30-120">DateTimeOffset</span></span>|<span data-ttu-id="92e30-121">Hora en la que se actualizó por última vez el estado de acción. Heredado de [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="92e30-121">Time the action state was last updated Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>|
|<span data-ttu-id="92e30-122">deviceLocation</span><span class="sxs-lookup"><span data-stu-id="92e30-122">deviceLocation</span></span>|[<span data-ttu-id="92e30-123">deviceGeoLocation</span><span class="sxs-lookup"><span data-stu-id="92e30-123">deviceGeoLocation</span></span>](../resources/intune_devices_devicegeolocation.md)|<span data-ttu-id="92e30-124">ubicación del dispositivo</span><span class="sxs-lookup"><span data-stu-id="92e30-124">device location</span></span>|

## <a name="relationships"></a><span data-ttu-id="92e30-125">Relaciones</span><span class="sxs-lookup"><span data-stu-id="92e30-125">Relationships</span></span>
<span data-ttu-id="92e30-126">Ninguna</span><span class="sxs-lookup"><span data-stu-id="92e30-126">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="92e30-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="92e30-127">JSON Representation</span></span>
<span data-ttu-id="92e30-128">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="92e30-128">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.locateDeviceActionResult"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.locateDeviceActionResult",
  "actionName": "String",
  "actionState": "String",
  "startDateTime": "String (timestamp)",
  "lastUpdatedDateTime": "String (timestamp)",
  "deviceLocation": {
    "@odata.type": "microsoft.graph.deviceGeoLocation",
    "lastCollectedDateTime": "String (timestamp)",
    "longitude": "<Unknown Primitive Type Edm.Double>",
    "latitude": "<Unknown Primitive Type Edm.Double>",
    "altitude": "<Unknown Primitive Type Edm.Double>",
    "horizontalAccuracy": "<Unknown Primitive Type Edm.Double>",
    "verticalAccuracy": "<Unknown Primitive Type Edm.Double>",
    "heading": "<Unknown Primitive Type Edm.Double>",
    "speed": "<Unknown Primitive Type Edm.Double>"
  }
}
```



