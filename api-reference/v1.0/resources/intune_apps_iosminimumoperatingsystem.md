# <a name="iosminimumoperatingsystem-resource-type"></a><span data-ttu-id="5aac2-101">Tipo de recurso iosMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="5aac2-101">iosMinimumOperatingSystem resource type</span></span>

> <span data-ttu-id="5aac2-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5aac2-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5aac2-103">Contiene las propiedades del sistema operativo mínimo necesario para una aplicación móvil de iOS.</span><span class="sxs-lookup"><span data-stu-id="5aac2-103">Contains properties of the minimum operating system required for an iOS mobile app.</span></span>
## <a name="properties"></a><span data-ttu-id="5aac2-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5aac2-104">Properties</span></span>
|<span data-ttu-id="5aac2-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5aac2-105">Property</span></span>|<span data-ttu-id="5aac2-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="5aac2-106">Type</span></span>|<span data-ttu-id="5aac2-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="5aac2-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5aac2-108">v8_0</span><span class="sxs-lookup"><span data-stu-id="5aac2-108">v8_0</span></span>|<span data-ttu-id="5aac2-109">Booleano</span><span class="sxs-lookup"><span data-stu-id="5aac2-109">Boolean</span></span>|<span data-ttu-id="5aac2-110">Versión 8.0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="5aac2-110">Version 8.0 or later.</span></span>|
|<span data-ttu-id="5aac2-111">v9_0</span><span class="sxs-lookup"><span data-stu-id="5aac2-111">v9_0</span></span>|<span data-ttu-id="5aac2-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="5aac2-112">Boolean</span></span>|<span data-ttu-id="5aac2-113">Versión 9.0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="5aac2-113">Version 9.0 or later.</span></span>|
|<span data-ttu-id="5aac2-114">v10_0</span><span class="sxs-lookup"><span data-stu-id="5aac2-114">v10_0</span></span>|<span data-ttu-id="5aac2-115">Booleano</span><span class="sxs-lookup"><span data-stu-id="5aac2-115">Boolean</span></span>|<span data-ttu-id="5aac2-116">Versión 10.0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="5aac2-116">Version 10.0 or later.</span></span>|
|<span data-ttu-id="5aac2-117">v11_0</span><span class="sxs-lookup"><span data-stu-id="5aac2-117">v11_0</span></span>|<span data-ttu-id="5aac2-118">Booleano</span><span class="sxs-lookup"><span data-stu-id="5aac2-118">Boolean</span></span>|<span data-ttu-id="5aac2-119">Versión 11.0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="5aac2-119">Version 11.0 or later.</span></span>|
|<span data-ttu-id="5aac2-120">v12_0</span><span class="sxs-lookup"><span data-stu-id="5aac2-120">v12_0</span></span>|<span data-ttu-id="5aac2-121">Booleano</span><span class="sxs-lookup"><span data-stu-id="5aac2-121">Boolean</span></span>|<span data-ttu-id="5aac2-122">Versión 12.0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="5aac2-122">Version 12.0 or later.</span></span>|

## <a name="relationships"></a><span data-ttu-id="5aac2-123">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5aac2-123">Relationships</span></span>
<span data-ttu-id="5aac2-124">Ninguna</span><span class="sxs-lookup"><span data-stu-id="5aac2-124">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="5aac2-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5aac2-125">JSON Representation</span></span>
<span data-ttu-id="5aac2-126">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5aac2-126">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosMinimumOperatingSystem"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosMinimumOperatingSystem",
  "v8_0": true,
  "v9_0": true,
  "v10_0": true,
  "v11_0": true,
  "v12_0": true
}
```



