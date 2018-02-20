# <a name="resetpasscodeactionresult-resource-type"></a><span data-ttu-id="f3749-101">Tipo de recurso resetPasscodeActionResult</span><span class="sxs-lookup"><span data-stu-id="f3749-101">resetPasscodeActionResult resource type</span></span>

> <span data-ttu-id="f3749-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f3749-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f3749-103">Resultado de la acción Restablecer código de acceso</span><span class="sxs-lookup"><span data-stu-id="f3749-103">Reset passcode action result</span></span>

<span data-ttu-id="f3749-104">Hereda de [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="f3749-104">Inherits from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>

## <a name="properties"></a><span data-ttu-id="f3749-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f3749-105">Properties</span></span>
|<span data-ttu-id="f3749-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f3749-106">Property</span></span>|<span data-ttu-id="f3749-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="f3749-107">Type</span></span>|<span data-ttu-id="f3749-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3749-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f3749-109">actionName</span><span class="sxs-lookup"><span data-stu-id="f3749-109">actionName</span></span>|<span data-ttu-id="f3749-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="f3749-110">String</span></span>|<span data-ttu-id="f3749-111">Nombre de la acción. Heredado de [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="f3749-111">Action name Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>|
|<span data-ttu-id="f3749-112">actionState</span><span class="sxs-lookup"><span data-stu-id="f3749-112">actionState</span></span>|<span data-ttu-id="f3749-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="f3749-113">String</span></span>|<span data-ttu-id="f3749-114">Estado de la acción. Heredado de [deviceActionResult](../resources/intune_devices_deviceactionresult.md). Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="f3749-114">State of the action Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md) Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="f3749-115">startDateTime</span><span class="sxs-lookup"><span data-stu-id="f3749-115">startDateTime</span></span>|<span data-ttu-id="f3749-116">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f3749-116">DateTimeOffset</span></span>|<span data-ttu-id="f3749-117">Hora en la que se inició la acción. Heredado de [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="f3749-117">Time the action was initiated Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>|
|<span data-ttu-id="f3749-118">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="f3749-118">lastUpdatedDateTime</span></span>|<span data-ttu-id="f3749-119">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f3749-119">DateTimeOffset</span></span>|<span data-ttu-id="f3749-120">Hora en la que se actualizó por última vez el estado de acción. Heredado de [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="f3749-120">Time the action state was last updated Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>|
|<span data-ttu-id="f3749-121">código de acceso</span><span class="sxs-lookup"><span data-stu-id="f3749-121">passcode</span></span>|<span data-ttu-id="f3749-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="f3749-122">String</span></span>|<span data-ttu-id="f3749-123">Código de acceso recién generado para el dispositivo</span><span class="sxs-lookup"><span data-stu-id="f3749-123">Newly generated passcode for the device</span></span> |

## <a name="relationships"></a><span data-ttu-id="f3749-124">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f3749-124">Relationships</span></span>
<span data-ttu-id="f3749-125">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f3749-125">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="f3749-126">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f3749-126">JSON Representation</span></span>
<span data-ttu-id="f3749-127">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f3749-127">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.resetPasscodeActionResult"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.resetPasscodeActionResult",
  "actionName": "String",
  "actionState": "String",
  "startDateTime": "String (timestamp)",
  "lastUpdatedDateTime": "String (timestamp)",
  "passcode": "String"
}
```



