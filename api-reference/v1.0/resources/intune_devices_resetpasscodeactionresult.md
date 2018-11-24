# <a name="resetpasscodeactionresult-resource-type"></a><span data-ttu-id="7a574-101">Tipo de recurso resetPasscodeActionResult</span><span class="sxs-lookup"><span data-stu-id="7a574-101">resetPasscodeActionResult resource type</span></span>

> <span data-ttu-id="7a574-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7a574-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7a574-103">Resultado de la acción Restablecer código de acceso</span><span class="sxs-lookup"><span data-stu-id="7a574-103">Reset passcode action result</span></span>

<span data-ttu-id="7a574-104">Hereda de [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="7a574-104">Inherits from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>

## <a name="properties"></a><span data-ttu-id="7a574-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7a574-105">Properties</span></span>
|<span data-ttu-id="7a574-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7a574-106">Property</span></span>|<span data-ttu-id="7a574-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="7a574-107">Type</span></span>|<span data-ttu-id="7a574-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a574-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7a574-109">actionName</span><span class="sxs-lookup"><span data-stu-id="7a574-109">actionName</span></span>|<span data-ttu-id="7a574-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="7a574-110">String</span></span>|<span data-ttu-id="7a574-111">Nombre de la acción. Heredado de [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="7a574-111">Action name Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>|
|<span data-ttu-id="7a574-112">actionState</span><span class="sxs-lookup"><span data-stu-id="7a574-112">actionState</span></span>|[<span data-ttu-id="7a574-113">actionState</span><span class="sxs-lookup"><span data-stu-id="7a574-113">actionState</span></span>](../resources/intune_devices_actionstate.md)|<span data-ttu-id="7a574-114">Estado de la acción Inherited desde [deviceActionResult](../resources/intune_devices_deviceactionresult.md).</span><span class="sxs-lookup"><span data-stu-id="7a574-114">State of the action Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md).</span></span> <span data-ttu-id="7a574-115">Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.</span><span class="sxs-lookup"><span data-stu-id="7a574-115">Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="7a574-116">startDateTime</span><span class="sxs-lookup"><span data-stu-id="7a574-116">startDateTime</span></span>|<span data-ttu-id="7a574-117">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7a574-117">DateTimeOffset</span></span>|<span data-ttu-id="7a574-118">Hora en la que se inició la acción. Heredado de [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="7a574-118">Time the action was initiated Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>|
|<span data-ttu-id="7a574-119">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="7a574-119">lastUpdatedDateTime</span></span>|<span data-ttu-id="7a574-120">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7a574-120">DateTimeOffset</span></span>|<span data-ttu-id="7a574-121">Hora en la que se actualizó por última vez el estado de acción. Heredado de [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="7a574-121">Time the action state was last updated Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>|
|<span data-ttu-id="7a574-122">código de acceso</span><span class="sxs-lookup"><span data-stu-id="7a574-122">passcode</span></span>|<span data-ttu-id="7a574-123">Cadena</span><span class="sxs-lookup"><span data-stu-id="7a574-123">String</span></span>|<span data-ttu-id="7a574-124">Código de acceso recién generado para el dispositivo</span><span class="sxs-lookup"><span data-stu-id="7a574-124">Newly generated passcode for the device</span></span> |

## <a name="relationships"></a><span data-ttu-id="7a574-125">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7a574-125">Relationships</span></span>
<span data-ttu-id="7a574-126">Ninguna</span><span class="sxs-lookup"><span data-stu-id="7a574-126">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="7a574-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7a574-127">JSON Representation</span></span>
<span data-ttu-id="7a574-128">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7a574-128">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
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



