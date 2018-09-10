# <a name="iosminimumoperatingsystem-resource-type"></a><span data-ttu-id="e9671-101">Tipo de recurso iosMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="e9671-101">iosMinimumOperatingSystem resource type</span></span>

> <span data-ttu-id="e9671-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e9671-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e9671-103">Contiene las propiedades del sistema operativo mínimo necesario para una aplicación móvil de iOS.</span><span class="sxs-lookup"><span data-stu-id="e9671-103">Contains properties of the minimum operating system required for an iOS mobile app.</span></span>
## <a name="properties"></a><span data-ttu-id="e9671-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e9671-104">Properties</span></span>
|<span data-ttu-id="e9671-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e9671-105">Property</span></span>|<span data-ttu-id="e9671-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="e9671-106">Type</span></span>|<span data-ttu-id="e9671-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9671-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e9671-108">v8_0</span><span class="sxs-lookup"><span data-stu-id="e9671-108">v8_0</span></span>|<span data-ttu-id="e9671-109">Booleano</span><span class="sxs-lookup"><span data-stu-id="e9671-109">Boolean</span></span>|<span data-ttu-id="e9671-110">Versión 8.0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="e9671-110">Version 8.0 or later.</span></span>|
|<span data-ttu-id="e9671-111">v9_0</span><span class="sxs-lookup"><span data-stu-id="e9671-111">v9_0</span></span>|<span data-ttu-id="e9671-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="e9671-112">Boolean</span></span>|<span data-ttu-id="e9671-113">Versión 9.0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="e9671-113">Version 9.0 or later.</span></span>|
|<span data-ttu-id="e9671-114">v10_0</span><span class="sxs-lookup"><span data-stu-id="e9671-114">v10_0</span></span>|<span data-ttu-id="e9671-115">Booleano</span><span class="sxs-lookup"><span data-stu-id="e9671-115">Boolean</span></span>|<span data-ttu-id="e9671-116">Versión 10.0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="e9671-116">Version 10.0 or later.</span></span>|
|<span data-ttu-id="e9671-117">v11_0</span><span class="sxs-lookup"><span data-stu-id="e9671-117">v11_0</span></span>|<span data-ttu-id="e9671-118">Booleano</span><span class="sxs-lookup"><span data-stu-id="e9671-118">Boolean</span></span>|<span data-ttu-id="e9671-119">Versión 11.0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="e9671-119">Version 11.0 or later.</span></span>|

## <a name="relationships"></a><span data-ttu-id="e9671-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e9671-120">Relationships</span></span>
<span data-ttu-id="e9671-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="e9671-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="e9671-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e9671-122">JSON Representation</span></span>
<span data-ttu-id="e9671-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e9671-123">Here is a JSON representation of the resource.</span></span>
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosMinimumOperatingSystem"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.iosMinimumOperatingSystem",
  "v8_0": true,
  "v9_0": true,
  "v10_0": true,
  "v11_0": true
}
```








