# <a name="updatewindowsdeviceaccountactionparameter-resource-type"></a><span data-ttu-id="7a546-101">Tipo de recurso updateWindowsDeviceAccountActionParameter</span><span class="sxs-lookup"><span data-stu-id="7a546-101">updateWindowsDeviceAccountActionParameter resource type</span></span>

> <span data-ttu-id="7a546-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7a546-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7a546-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="7a546-103">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="7a546-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7a546-104">Properties</span></span>
|<span data-ttu-id="7a546-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7a546-105">Property</span></span>|<span data-ttu-id="7a546-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="7a546-106">Type</span></span>|<span data-ttu-id="7a546-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a546-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7a546-108">deviceAccount</span><span class="sxs-lookup"><span data-stu-id="7a546-108">deviceAccount</span></span>|[<span data-ttu-id="7a546-109">windowsDeviceAccount</span><span class="sxs-lookup"><span data-stu-id="7a546-109">windowsDeviceAccount</span></span>](../resources/intune_devices_windowsdeviceaccount.md)|<span data-ttu-id="7a546-110">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="7a546-110">Not yet documented</span></span>|
|<span data-ttu-id="7a546-111">passwordRotationEnabled</span><span class="sxs-lookup"><span data-stu-id="7a546-111">passwordRotationEnabled</span></span>|<span data-ttu-id="7a546-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="7a546-112">Boolean</span></span>|<span data-ttu-id="7a546-113">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="7a546-113">Not yet documented</span></span>|
|<span data-ttu-id="7a546-114">calendarSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="7a546-114">calendarSyncEnabled</span></span>|<span data-ttu-id="7a546-115">Booleano</span><span class="sxs-lookup"><span data-stu-id="7a546-115">Boolean</span></span>|<span data-ttu-id="7a546-116">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="7a546-116">Not yet documented</span></span>|
|<span data-ttu-id="7a546-117">deviceAccountEmail</span><span class="sxs-lookup"><span data-stu-id="7a546-117">deviceAccountEmail</span></span>|<span data-ttu-id="7a546-118">cadena</span><span class="sxs-lookup"><span data-stu-id="7a546-118">String</span></span>|<span data-ttu-id="7a546-119">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="7a546-119">Not yet documented</span></span>|
|<span data-ttu-id="7a546-120">exchangeServer</span><span class="sxs-lookup"><span data-stu-id="7a546-120">exchangeServer</span></span>|<span data-ttu-id="7a546-121">cadena</span><span class="sxs-lookup"><span data-stu-id="7a546-121">String</span></span>|<span data-ttu-id="7a546-122">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="7a546-122">Not yet documented</span></span>|
|<span data-ttu-id="7a546-123">sessionInitiationProtocalAddress</span><span class="sxs-lookup"><span data-stu-id="7a546-123">sessionInitiationProtocalAddress</span></span>|<span data-ttu-id="7a546-124">cadena</span><span class="sxs-lookup"><span data-stu-id="7a546-124">String</span></span>|<span data-ttu-id="7a546-125">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="7a546-125">Not yet documented</span></span>|

## <a name="relationships"></a><span data-ttu-id="7a546-126">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7a546-126">Relationships</span></span>
<span data-ttu-id="7a546-127">Ninguna</span><span class="sxs-lookup"><span data-stu-id="7a546-127">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="7a546-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7a546-128">JSON Representation</span></span>
<span data-ttu-id="7a546-129">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7a546-129">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.updateWindowsDeviceAccountActionParameter"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.updateWindowsDeviceAccountActionParameter",
  "deviceAccount": {
    "@odata.type": "microsoft.graph.windowsDeviceAccount",
    "password": "String"
  },
  "passwordRotationEnabled": true,
  "calendarSyncEnabled": true,
  "deviceAccountEmail": "String",
  "exchangeServer": "String",
  "sessionInitiationProtocalAddress": "String"
}
```



