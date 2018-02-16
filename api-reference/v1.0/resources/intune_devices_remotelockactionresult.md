# <a name="remotelockactionresult-resource-type"></a><span data-ttu-id="8c0c1-101">Tipo de recurso remoteLockActionResult</span><span class="sxs-lookup"><span data-stu-id="8c0c1-101">remoteLockActionResult resource type</span></span>

> <span data-ttu-id="8c0c1-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8c0c1-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8c0c1-103">Bloquear el resultado de la acción con un PIN de desbloqueo</span><span class="sxs-lookup"><span data-stu-id="8c0c1-103">Lock action result with a pin to unlock</span></span>

<span data-ttu-id="8c0c1-104">Hereda de [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="8c0c1-104">Inherits from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>

## <a name="properties"></a><span data-ttu-id="8c0c1-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8c0c1-105">Properties</span></span>
|<span data-ttu-id="8c0c1-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8c0c1-106">Property</span></span>|<span data-ttu-id="8c0c1-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="8c0c1-107">Type</span></span>|<span data-ttu-id="8c0c1-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c0c1-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8c0c1-109">actionName</span><span class="sxs-lookup"><span data-stu-id="8c0c1-109">actionName</span></span>|<span data-ttu-id="8c0c1-110">cadena</span><span class="sxs-lookup"><span data-stu-id="8c0c1-110">String</span></span>|<span data-ttu-id="8c0c1-111">Nombre de la acción. Heredado de [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="8c0c1-111">Action name Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>|
|<span data-ttu-id="8c0c1-112">actionState</span><span class="sxs-lookup"><span data-stu-id="8c0c1-112">actionState</span></span>|<span data-ttu-id="8c0c1-113">cadena</span><span class="sxs-lookup"><span data-stu-id="8c0c1-113">String</span></span>|<span data-ttu-id="8c0c1-114">Estado de la acción. Heredado de [deviceActionResult](../resources/intune_devices_deviceactionresult.md). Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="8c0c1-114">State of the action Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md) Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="8c0c1-115">startDateTime</span><span class="sxs-lookup"><span data-stu-id="8c0c1-115">startDateTime</span></span>|<span data-ttu-id="8c0c1-116">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8c0c1-116">DateTimeOffset</span></span>|<span data-ttu-id="8c0c1-117">Hora en la que se inició la acción. Heredado de [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="8c0c1-117">Time the action was initiated Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>|
|<span data-ttu-id="8c0c1-118">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="8c0c1-118">lastUpdatedDateTime</span></span>|<span data-ttu-id="8c0c1-119">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8c0c1-119">DateTimeOffset</span></span>|<span data-ttu-id="8c0c1-120">Hora en la que se actualizó por última vez el estado de acción. Heredado de [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="8c0c1-120">Time the action state was last updated Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>|
|<span data-ttu-id="8c0c1-121">unlockPin</span><span class="sxs-lookup"><span data-stu-id="8c0c1-121">unlockPin</span></span>|<span data-ttu-id="8c0c1-122">cadena</span><span class="sxs-lookup"><span data-stu-id="8c0c1-122">String</span></span>|<span data-ttu-id="8c0c1-123">PIN para desbloquear el cliente</span><span class="sxs-lookup"><span data-stu-id="8c0c1-123">Pin to unlock the client</span></span>|

## <a name="relationships"></a><span data-ttu-id="8c0c1-124">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8c0c1-124">Relationships</span></span>
<span data-ttu-id="8c0c1-125">Ninguna</span><span class="sxs-lookup"><span data-stu-id="8c0c1-125">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="8c0c1-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8c0c1-126">JSON Representation</span></span>
<span data-ttu-id="8c0c1-127">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8c0c1-127">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.remoteLockActionResult"
}
-->
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



