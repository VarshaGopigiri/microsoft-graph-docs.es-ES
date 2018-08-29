# <a name="remotelockactionresult-resource-type"></a><span data-ttu-id="66ae9-101">Tipo de recurso remoteLockActionResult</span><span class="sxs-lookup"><span data-stu-id="66ae9-101">remoteLockActionResult resource type</span></span>

> <span data-ttu-id="66ae9-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="66ae9-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="66ae9-103">Bloquear el resultado de la acción con un PIN de desbloqueo</span><span class="sxs-lookup"><span data-stu-id="66ae9-103">Lock action result with a pin to unlock</span></span>

<span data-ttu-id="66ae9-104">Hereda de [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="66ae9-104">Inherits from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>

## <a name="properties"></a><span data-ttu-id="66ae9-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="66ae9-105">Properties</span></span>
|<span data-ttu-id="66ae9-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="66ae9-106">Property</span></span>|<span data-ttu-id="66ae9-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="66ae9-107">Type</span></span>|<span data-ttu-id="66ae9-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="66ae9-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="66ae9-109">actionName</span><span class="sxs-lookup"><span data-stu-id="66ae9-109">actionName</span></span>|<span data-ttu-id="66ae9-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="66ae9-110">String</span></span>|<span data-ttu-id="66ae9-111">Nombre de la acción. Heredado de [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="66ae9-111">Action name Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>|
|<span data-ttu-id="66ae9-112">actionState</span><span class="sxs-lookup"><span data-stu-id="66ae9-112">actionState</span></span>|[<span data-ttu-id="66ae9-113">actionState</span><span class="sxs-lookup"><span data-stu-id="66ae9-113">actionState</span></span>](../resources/intune_devices_actionstate.md)|<span data-ttu-id="66ae9-114">Estado de la acción Inherited desde [deviceActionResult](../resources/intune_devices_deviceactionresult.md).</span><span class="sxs-lookup"><span data-stu-id="66ae9-114">State of the action Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md) Possible values are: , , , , , , .</span></span> <span data-ttu-id="66ae9-115">Los valores posibles son `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="66ae9-115">The possible values are `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`, , , , , or .</span></span>|
|<span data-ttu-id="66ae9-116">startDateTime</span><span class="sxs-lookup"><span data-stu-id="66ae9-116">startDateTime</span></span>|<span data-ttu-id="66ae9-117">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="66ae9-117">DateTimeOffset</span></span>|<span data-ttu-id="66ae9-118">Hora en la que se inició la acción. Heredado de [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="66ae9-118">Time the action was initiated Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>|
|<span data-ttu-id="66ae9-119">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="66ae9-119">lastUpdatedDateTime</span></span>|<span data-ttu-id="66ae9-120">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="66ae9-120">DateTimeOffset</span></span>|<span data-ttu-id="66ae9-121">Hora en la que se actualizó por última vez el estado de acción. Heredado de [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="66ae9-121">Time the action state was last updated Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>|
|<span data-ttu-id="66ae9-122">unlockPin</span><span class="sxs-lookup"><span data-stu-id="66ae9-122">unlockPin</span></span>|<span data-ttu-id="66ae9-123">cadena</span><span class="sxs-lookup"><span data-stu-id="66ae9-123">String</span></span>|<span data-ttu-id="66ae9-124">PIN para desbloquear el cliente</span><span class="sxs-lookup"><span data-stu-id="66ae9-124">Pin to unlock the client</span></span>|

## <a name="relationships"></a><span data-ttu-id="66ae9-125">Relaciones</span><span class="sxs-lookup"><span data-stu-id="66ae9-125">Relationships</span></span>
<span data-ttu-id="66ae9-126">Ninguna</span><span class="sxs-lookup"><span data-stu-id="66ae9-126">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="66ae9-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="66ae9-127">JSON Representation</span></span>
<span data-ttu-id="66ae9-128">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="66ae9-128">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.deviceActionResult",
  "@odata.type": "microsoft.graph.remoteLockActionResult"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.remoteLockActionResult",
  "actionName": "String",
  "actionState": "String",
  "startDateTime": "String (timestamp)",
  "lastUpdatedDateTime": "String (timestamp)",
  "unlockPin": "String"
}
```



