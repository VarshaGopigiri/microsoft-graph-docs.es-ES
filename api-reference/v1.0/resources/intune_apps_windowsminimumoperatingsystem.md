# <a name="windowsminimumoperatingsystem-resource-type"></a><span data-ttu-id="419ff-101">Tipo de recurso windowsMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="419ff-101">windowsMinimumOperatingSystem resource type</span></span>

> <span data-ttu-id="419ff-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="419ff-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="419ff-103">El sistema operativo mínimo necesario para una aplicación móvil de Windows.</span><span class="sxs-lookup"><span data-stu-id="419ff-103">The minimum operating system required for a Windows mobile app.</span></span>
## <a name="properties"></a><span data-ttu-id="419ff-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="419ff-104">Properties</span></span>
|<span data-ttu-id="419ff-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="419ff-105">Property</span></span>|<span data-ttu-id="419ff-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="419ff-106">Type</span></span>|<span data-ttu-id="419ff-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="419ff-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="419ff-108">v8_0</span><span class="sxs-lookup"><span data-stu-id="419ff-108">v8_0</span></span>|<span data-ttu-id="419ff-109">Booleano</span><span class="sxs-lookup"><span data-stu-id="419ff-109">Boolean</span></span>|<span data-ttu-id="419ff-110">Windows versión 8.0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="419ff-110">Windows version 8.0 or later.</span></span>|
|<span data-ttu-id="419ff-111">v8_1</span><span class="sxs-lookup"><span data-stu-id="419ff-111">v8_1</span></span>|<span data-ttu-id="419ff-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="419ff-112">Boolean</span></span>|<span data-ttu-id="419ff-113">Windows versión 8.1 o posterior.</span><span class="sxs-lookup"><span data-stu-id="419ff-113">Windows version 8.1 or later.</span></span>|
|<span data-ttu-id="419ff-114">v10_0</span><span class="sxs-lookup"><span data-stu-id="419ff-114">v10_0</span></span>|<span data-ttu-id="419ff-115">Booleano</span><span class="sxs-lookup"><span data-stu-id="419ff-115">Boolean</span></span>|<span data-ttu-id="419ff-116">Windows versión 10.0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="419ff-116">Windows version 10.0 or later.</span></span>|

## <a name="relationships"></a><span data-ttu-id="419ff-117">Relaciones</span><span class="sxs-lookup"><span data-stu-id="419ff-117">Relationships</span></span>
<span data-ttu-id="419ff-118">Ninguna</span><span class="sxs-lookup"><span data-stu-id="419ff-118">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="419ff-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="419ff-119">JSON Representation</span></span>
<span data-ttu-id="419ff-120">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="419ff-120">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsMinimumOperatingSystem"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsMinimumOperatingSystem",
  "v8_0": true,
  "v8_1": true,
  "v10_0": true
}
```



