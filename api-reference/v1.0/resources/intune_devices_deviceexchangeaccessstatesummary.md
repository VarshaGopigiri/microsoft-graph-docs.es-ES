# <a name="deviceexchangeaccessstatesummary-resource-type"></a><span data-ttu-id="704d0-101">Tipo de recurso deviceExchangeAccessStateSummary</span><span class="sxs-lookup"><span data-stu-id="704d0-101">deviceExchangeAccessStateSummary resource type</span></span>

> <span data-ttu-id="704d0-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="704d0-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="704d0-103">Resumen del estado de acceso del dispositivo a Exchange</span><span class="sxs-lookup"><span data-stu-id="704d0-103">Device Exchange Access State summary</span></span>
## <a name="properties"></a><span data-ttu-id="704d0-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="704d0-104">Properties</span></span>
|<span data-ttu-id="704d0-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="704d0-105">Property</span></span>|<span data-ttu-id="704d0-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="704d0-106">Type</span></span>|<span data-ttu-id="704d0-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="704d0-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="704d0-108">allowedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="704d0-108">allowedDeviceCount</span></span>|<span data-ttu-id="704d0-109">Int32</span><span class="sxs-lookup"><span data-stu-id="704d0-109">Int32</span></span>|<span data-ttu-id="704d0-110">Número total de dispositivos con el estado de acceso de Exchange: Permitido.</span><span class="sxs-lookup"><span data-stu-id="704d0-110">Total count of devices with Exchange Access State: Allowed.</span></span>|
|<span data-ttu-id="704d0-111">blockedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="704d0-111">blockedDeviceCount</span></span>|<span data-ttu-id="704d0-112">Int32</span><span class="sxs-lookup"><span data-stu-id="704d0-112">Int32</span></span>|<span data-ttu-id="704d0-113">Número total de dispositivos con el estado de acceso de Exchange: Bloqueado.</span><span class="sxs-lookup"><span data-stu-id="704d0-113">Total count of devices with Exchange Access State: Blocked.</span></span>|
|<span data-ttu-id="704d0-114">quarantinedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="704d0-114">quarantinedDeviceCount</span></span>|<span data-ttu-id="704d0-115">Int32</span><span class="sxs-lookup"><span data-stu-id="704d0-115">Int32</span></span>|<span data-ttu-id="704d0-116">Número total de dispositivos con el estado de acceso de Exchange: En cuarentena.</span><span class="sxs-lookup"><span data-stu-id="704d0-116">Total count of devices with Exchange Access State: Quarantined.</span></span>|
|<span data-ttu-id="704d0-117">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="704d0-117">unknownDeviceCount</span></span>|<span data-ttu-id="704d0-118">Int32</span><span class="sxs-lookup"><span data-stu-id="704d0-118">Int32</span></span>|<span data-ttu-id="704d0-119">Número total de dispositivos con el estado de acceso de Exchange: Desconocido.</span><span class="sxs-lookup"><span data-stu-id="704d0-119">Total count of devices with Exchange Access State: Unknown.</span></span>|
|<span data-ttu-id="704d0-120">unavailableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="704d0-120">unavailableDeviceCount</span></span>|<span data-ttu-id="704d0-121">Int32</span><span class="sxs-lookup"><span data-stu-id="704d0-121">Int32</span></span>|<span data-ttu-id="704d0-122">Número total de dispositivos para los que no se puede encontrar el estado de acceso de Exchange.</span><span class="sxs-lookup"><span data-stu-id="704d0-122">Total count of devices for which no Exchange Access State could be found.</span></span>|

## <a name="relationships"></a><span data-ttu-id="704d0-123">Relaciones</span><span class="sxs-lookup"><span data-stu-id="704d0-123">Relationships</span></span>
<span data-ttu-id="704d0-124">Ninguna</span><span class="sxs-lookup"><span data-stu-id="704d0-124">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="704d0-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="704d0-125">JSON Representation</span></span>
<span data-ttu-id="704d0-126">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="704d0-126">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceExchangeAccessStateSummary"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceExchangeAccessStateSummary",
  "allowedDeviceCount": 1024,
  "blockedDeviceCount": 1024,
  "quarantinedDeviceCount": 1024,
  "unknownDeviceCount": 1024,
  "unavailableDeviceCount": 1024
}
```



