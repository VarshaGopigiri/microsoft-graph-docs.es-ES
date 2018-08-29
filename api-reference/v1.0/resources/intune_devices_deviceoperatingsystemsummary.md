# <a name="deviceoperatingsystemsummary-resource-type"></a><span data-ttu-id="14742-101">Tipo de recurso deviceOperatingSystemSummary</span><span class="sxs-lookup"><span data-stu-id="14742-101">deviceOperatingSystemSummary resource type</span></span>

> <span data-ttu-id="14742-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="14742-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="14742-103">Resumen de sistemas operativos de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="14742-103">Device operating system summary.</span></span>
## <a name="properties"></a><span data-ttu-id="14742-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="14742-104">Properties</span></span>
|<span data-ttu-id="14742-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="14742-105">Property</span></span>|<span data-ttu-id="14742-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="14742-106">Type</span></span>|<span data-ttu-id="14742-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="14742-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="14742-108">androidCount</span><span class="sxs-lookup"><span data-stu-id="14742-108">androidCount</span></span>|<span data-ttu-id="14742-109">Int32</span><span class="sxs-lookup"><span data-stu-id="14742-109">Int32</span></span>|<span data-ttu-id="14742-110">Número del recuento de dispositivos Android.</span><span class="sxs-lookup"><span data-stu-id="14742-110">Number of android device count.</span></span>|
|<span data-ttu-id="14742-111">iosCount</span><span class="sxs-lookup"><span data-stu-id="14742-111">iosCount</span></span>|<span data-ttu-id="14742-112">Int32</span><span class="sxs-lookup"><span data-stu-id="14742-112">Int32</span></span>|<span data-ttu-id="14742-113">Número del recuento de dispositivos iOS.</span><span class="sxs-lookup"><span data-stu-id="14742-113">Number of iOS device count.</span></span>|
|<span data-ttu-id="14742-114">macOSCount</span><span class="sxs-lookup"><span data-stu-id="14742-114">macOSCount</span></span>|<span data-ttu-id="14742-115">Int32</span><span class="sxs-lookup"><span data-stu-id="14742-115">Int32</span></span>|<span data-ttu-id="14742-116">Número del recuento de dispositivos Mac OS X.</span><span class="sxs-lookup"><span data-stu-id="14742-116">Number of Mac OS X device count.</span></span>|
|<span data-ttu-id="14742-117">windowsMobileCount</span><span class="sxs-lookup"><span data-stu-id="14742-117">windowsMobileCount</span></span>|<span data-ttu-id="14742-118">Int32</span><span class="sxs-lookup"><span data-stu-id="14742-118">Int32</span></span>|<span data-ttu-id="14742-119">Número del recuento de dispositivos móviles Windows.</span><span class="sxs-lookup"><span data-stu-id="14742-119">Number of Windows mobile device count.</span></span>|
|<span data-ttu-id="14742-120">windowsCount</span><span class="sxs-lookup"><span data-stu-id="14742-120">windowsCount</span></span>|<span data-ttu-id="14742-121">Int32</span><span class="sxs-lookup"><span data-stu-id="14742-121">Int32</span></span>|<span data-ttu-id="14742-122">Número del recuento de dispositivos Windows.</span><span class="sxs-lookup"><span data-stu-id="14742-122">Number of Windows device count.</span></span>|
|<span data-ttu-id="14742-123">unknownCount</span><span class="sxs-lookup"><span data-stu-id="14742-123">unknownCount</span></span>|<span data-ttu-id="14742-124">Int32</span><span class="sxs-lookup"><span data-stu-id="14742-124">Int32</span></span>|<span data-ttu-id="14742-125">Número del recuento de dispositivos desconocidos.</span><span class="sxs-lookup"><span data-stu-id="14742-125">Number of unknown device count.</span></span>|

## <a name="relationships"></a><span data-ttu-id="14742-126">Relaciones</span><span class="sxs-lookup"><span data-stu-id="14742-126">Relationships</span></span>
<span data-ttu-id="14742-127">Ninguna</span><span class="sxs-lookup"><span data-stu-id="14742-127">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="14742-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="14742-128">JSON Representation</span></span>
<span data-ttu-id="14742-129">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="14742-129">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceOperatingSystemSummary"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceOperatingSystemSummary",
  "androidCount": 1024,
  "iosCount": 1024,
  "macOSCount": 1024,
  "windowsMobileCount": 1024,
  "windowsCount": 1024,
  "unknownCount": 1024
}
```



